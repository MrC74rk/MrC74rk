//
//  ContentView.swift
//  MrC74rk.me
//
//  Created by MrC74rk on 4/21/21.
//

import SwiftUI
// import Beer

struct ContentView: View {
    @State private var isPresented = false
    var body: some View {
        VStack{
            Spacer()
            HomeView(isPresented: $isPresented, selection: self.$selection)
            Spacer()
        }
        .frame(maxWidth: .infinity, maxHeight: .infinity)
        .ignoresSafeArea(.all)
        .foregroundColor(.white)
        .sheet(isPresented: $isPresented, content: {
            SideMenuView(isPresented: $isPresented)
        })
    }
}

struct HomeView: View {
   @Binding var isPresented: Bool

    var body: some View {  
        ZStack {
            VStack {
                VStack {
                    
                    Text("HOWDY!").font(.system(size:30))
             
                }
                .padding()
                  Button(action: {
                      isPresented.toggle()
                      }) {
                      Image("myLogo")
                          .resizable()
                          .frame(width: 50, height:28.79)
                          .opacity(0.1)
                          .padding(60)
                  }

  }
}

<!---
MrC74rk/MrC74rk is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
