#include <iostream>
using namespace std;

string gwarden,jwarden,ywarden;
int gsalary,jsalary,ysalary;

struct details{
    int check;
    string name,adn,dob;
};

struct student{
    int room,pay;
    long long int fees;
    string adn,name,dob,hname,ac,sharing;
};

struct ganga{
    details n1[1];
};
struct jamuna{
    details n2[2];
};

struct yamuna{
    details n3[3];
};

student s[300];
ganga g[5][10];
jamuna J[5][10];
yamuna y[5][10];

void payfee(int index1){
    int choice;
    if(s[index1].pay==NULL){
        l3:
        cout<<"fee to be paid is:"<<s[index1].fees<<endl;
        cout<<"would you like to pay the fee:\n1)yes\n2)no\n";
        cin>>choice;
        switch(choice){
            case 1:
            s[index1].pay=1;
            break;
            case 2:
            cout<<"please pay the fee as soon as possible";
            break;
            default:
            goto l3;
        }
        
    }
    else{
        cout<<"fees has already been paid";
    }
}

void check_floor_status1(int n){
    int i,j,k,flag;
    for(i=n;i<5;i+=2){
        flag=0;
        for(j=0;j<10;j++){
            if(g[i][j].n1[0].check==NULL){
                    cout<<((i+1)*100)+(j+1)<<"  ";
            }
        }
        cout<<endl;
    }
}

void GANGA(int index1){
    int choice,room;
    l5:
    cout<<"choose the type of room:\n";
    cout<<"1)A/C \n2)non-A/C"<<endl;
    cin>>choice;
    if(choice==1){
        cout<<"choose your room:"<<endl;
        check_floor_status1(0);
        cin>>room;
        if(g[room/100-1][room%100-1].n1[0].check==NULL){
            s[index1].fees=3*50000;
            s[index1].room=room;
            s[index1].hname="GANGA";
            s[index1].ac="A/C";
            g[room/100-1][room%100-1].n1[0].check=1;
        }
        else{
            cout<<"the room is not vacant\nplease choose another room\n";
            goto l5;
        }
    }
    else{
        cout<<"choose your room:"<<endl;
        check_floor_status1(1);
        cin>>room;
        if(g[room/100-1][room%100-1].n1[0].check==NULL){
            s[index1].fees=3*50000;
            s[index1].room=room;
            s[index1].hname="GANGA";
            s[index1].ac="NON A/C";
            g[room/100-1][room%100-1].n1[0].check=1;
            g[room/100-1][room%100-1].n1[0].name=s[index1].name;
            g[room/100-1][room%100-1].n1[0].dob=s[index1].dob;
            g[room/100-1][room%100-1].n1[0].adn=s[index1].adn;
        }
        else{
            cout<<"the room is not vacant\nplease choose another room\n";
            goto l5;
        }
    }
    payfee(index1);
}

void check_floor_status2(int n){
    int i,j,k,flag;
    for(i=n;i<5;i+=2){
        flag=0;
        for(j=0;j<10;j++){
            for(k=0;k<2;k++){
                if(J[i][j].n2[k].check==NULL){
                        cout<<((i+1)*100)+(j+1)<<"  ";
                        break;
                }
            }
        }
        cout<<endl;
    }
}

void JAMUNA(int index1){
    int choice,room,i,flag=1;
    l6:
    cout<<"choose the type of room:\n";
    cout<<"1)A/C \n2)non-A/C"<<endl;
    cin>>choice;
    if(choice==1){
        cout<<"choose your room:"<<endl;
        check_floor_status2(0);
        cin>>room;
        s[index1].fees=2*50000;
        s[index1].room=room;
        for(i=0;i<2;i++){
            if(J[room/100-1][room%100-1].n2[i].check==NULL){
                flag=0;
                s[index1].hname="JAMUNA";
                s[index1].ac="A/C";
                J[room/100-1][room%100-1].n2[i].check=1;
                J[room/100-1][room%100-1].n2[i].name=s[index1].name;
                J[room/100-1][room%100-1].n2[i].dob=s[index1].dob;
                J[room/100-1][room%100-1].n2[i].adn=s[index1].adn;
                break;
            }
        }
        if(flag){
            cout<<"the room is not vacant\nplease choose another room\n";
            goto l6;
        }
    }
    else{
        cout<<"choose your room:"<<endl;
        check_floor_status2(1);
        cin>>room;
        s[index1].fees=3*50000;
        s[index1].room=room;
        for(i=0;i<2;i++){
            if(J[room/100-1][room%100-1].n2[i].check==NULL){
                flag=0;
                s[index1].hname="JAMUNA";
                s[index1].ac="NON A/C";
                J[room/100-1][room%100-1].n2[i].check=1;
                J[room/100-1][room%100-1].n2[i].name=s[index1].name;
                J[room/100-1][room%100-1].n2[i].dob=s[index1].dob;
                J[room/100-1][room%100-1].n2[i].adn=s[index1].adn;
                break;
            }
        }
        if(flag){
            cout<<"the room is not vacant\nplease choose another room\n";
            goto l6;
        }
        
    }
    payfee(index1);
}

void check_floor_status3(int n){
    int i,j,k,flag;
    for(i=n;i<5;i+=2){
        flag=0;
        for(j=0;j<10;j++){
            for(k=0;k<3;k++){
                if(y[i][j].n3[k].check==NULL){
                        cout<<((i+1)*100)+(j+1)<<"  ";
                        break;
                }
            }
        }
        cout<<endl;
    }
}

void YAMUNA(int index1){
    int choice,room,i,flag=1;
    l7:
    cout<<"choose the type of room:\n";
    cout<<"1)A/C \n2)non-A/C"<<endl;
    cin>>choice;
    if(choice==1){
        cout<<"choose your room:"<<endl;
        check_floor_status3(0);
        cin>>room;
        s[index1].fees=50000;
        s[index1].room=room;
        for(i=0;i<3;i++){
            if(y[room/100-1][room%100-1].n3[i].check==NULL){
                flag=0;
                s[index1].hname="YAMUNA";
                s[index1].ac="A/C";
                y[room/100-1][room%100-1].n3[i].check=1;
                y[room/100-1][room%100-1].n3[i].name=s[index1].name;
                y[room/100-1][room%100-1].n3[i].dob=s[index1].dob;
                y[room/100-1][room%100-1].n3[i].adn=s[index1].adn;
                break;
            }
        }
        if(flag){
            cout<<"the room is not vacant\nplease choose another room\n";
            goto l7;
        }
    }
    else{
        cout<<"choose your room:"<<endl;
        check_floor_status3(1);
        cin>>room;
        s[index1].fees=50000;
        s[index1].room=room;
        for(i=0;i<3;i++){
            if(y[room/100-1][room%100-1].n3[i].check==NULL){
                flag=0;
                s[index1].hname="YAMUNA";
                s[index1].ac="NON A/C";
                y[room/100-1][room%100-1].n3[i].check=1;
                y[room/100-1][room%100-1].n3[i].name=s[index1].name;
                y[room/100-1][room%100-1].n3[i].dob=s[index1].dob;
                y[room/100-1][room%100-1].n3[i].adn=s[index1].adn;
                break;
            }
        }
        if(flag){
            cout<<"the room is not vacant\nplease choose another room\n";
            goto l7;
        }
    }
    payfee(index1);
}

void BOOK2(int index1){
    int choice;
    l4:
    cout<<"choose the type of room:"<<endl;
    cout<<"1)single sharing\n2)double sharing\n3)triple sharing"<<endl;
    cin>>choice;
    switch(choice){
        case 1:
        s[index1].sharing="single sharing";
        GANGA(index1);
        break;
        case 2:
        s[index1].sharing="double sharing";
        JAMUNA(index1);
        break;
        case 3:
        s[index1].sharing="triple sharing";
        YAMUNA(index1);
        break;
        default:
        cout<<"invalid choice\nplease enter a valid option"<<endl;
        goto l4;
    }
}

int book(int index1){
    int choice;
    if(s[index1].room!=NULL){
        cout<<"you have already booked a room"<<endl;
        if(s[index1].pay==NULL){
            cout<<"you haven't paid the fee yet"<<endl;
            l2:
            cout<<"would you like to continue to fee payment:\n";
            cout<<"1)yes\n2)no\n";
            cin>>choice;
            switch(choice){
                case 1:
                payfee(index1);
                break;
                case 2:
                return 0;
                break;
                default:
                cout<<"invalid option\nchoose again\n";
                goto l2;
            }
        }
    }
    else{
        BOOK2(index1);
    }
    
}

void roomate_details(int index1){
    int i,j,k,flag=1;
    i=(s[index1].room/100)-1;
    j=(s[index1].room%100)-1;
    if(s[index1].hname=="JAMUNA"){
        for(k=0;k<2;k++){
            if(J[i][j].n2[k].check!=NULL && J[i][j].n2[k].adn!=s[index1].adn){
                flag=0;
                cout<<"name:"<<J[i][j].n2[k].name<<endl;
                cout<<"admission number:"<<J[i][j].n2[k].adn<<endl;
                cout<<"date of birth:"<<J[i][j].n2[k].dob<<endl;
            }
        }
    }
    else if(s[index1].hname=="YAMUNA"){
        for(k=0;k<3;k++){
            if(y[i][j].n3[k].check!=NULL && y[i][j].n3[k].adn!=s[index1].adn){
                flag=0;
                cout<<"name:"<<y[i][j].n3[k].name<<endl;
                cout<<"admission number:"<<y[i][j].n3[k].adn<<endl;
                cout<<"date of birth:"<<y[i][j].n3[k].dob<<endl;
            }
        }
    }
    if(flag){
        cout<<"no roomates yet";
    }
}

void status(int index1){
    int choice,i,j,k,flag=1;
    cout<<"name:"<<s[index1].name<<endl;
    cout<<"admission number:"<<s[index1].adn<<endl;
    cout<<"date of birth:"<<s[index1].dob<<endl;
    if(s[index1].room!=NULL){
        cout<<"hostel name:"<<s[index1].hname<<endl;
        cout<<"room number:"<<s[index1].room<<endl;
        cout<<"conditioning:"<<s[index1].ac<<endl;
        cout<<"hostel fee:"<<s[index1].fees<<"/-"<<endl;
        if(s[index1].pay!=NULL){
            cout<<"fee paid"<<endl;
        }
        else{
            cout<<"fee not yet paid"<<endl;
        }
        cout<<"room type: "<<s[index1].sharing<<endl;
    }
    else{
        cout<<"room not yet booked"<<endl;
    }
}

void clear_details(int index1){
    int i,j,k;
    i=(s[index1].room/100)-1;
    j=(s[index1].room%100)-1;
    if(s[index1].hname=="GANGA"){
        g[i][j].n1[0].check=0;
        g[i][j].n1[0].name="0";
        g[i][j].n1[0].dob="0";
        g[i][j].n1[0].adn="0";
    }
    else if(s[index1].hname=="JAMUNA"){
        for(k=0;k<2;k++){
            if(J[i][j].n2[k].adn==s[index1].adn){
                J[i][j].n2[k].check=0;
                J[i][j].n2[k].name="0";
                J[i][j].n2[k].dob="0";
                J[i][j].n2[k].adn="0";
            }
        }
    }
    else if(s[index1].hname=="YAMUNA"){
        for(k=0;k<3;k++){
            if(y[i][j].n3[k].adn==s[index1].adn){
                y[i][j].n3[k].check=0;
                y[i][j].n3[k].name="0";
                y[i][j].n3[k].dob="0";
                y[i][j].n3[k].adn="0";
            }
        }
    }
    s[index1].room=0;
    s[index1].pay=0;
    s[index1].fees=0;
    s[index1].hname="0";
    s[index1].ac="0";
    s[index1].sharing="0";
}

void change(int index1){
    int choice;
    if(s[index1].room!=NULL){
        cout<<"present details"<<endl;
        status(index1);
        cout<<"would you like to change your room"<<"1)YES\n2)NO"<<endl;
        cin>>choice;
        if(choice==1){
            cout<<"please choose your new room:"<<endl;
            clear_details(index1);
            book(index1);
        }
        else if(choice==2){
            cout<<"room not changed!"<<endl;
        }
    }
    else{
        cout<<"room not booked yet"<<endl;
    }
}

void vacate(int index1){
    int choice;
    if(s[index1].room!=NULL){
        status(index1);
        cout<<"Do you want to vacate the room"<<endl<<"1)YES\n2)NO"<<endl;
        cin>>choice;
        if(choice==1){
            clear_details(index1);
            cout<<"room successfully vacated"<<endl;
        }
        else if(choice==2){
            cout<<"room not vacated"<<endl;
        }
    }
    else{
        cout<<"room has not been booked yet"<<endl;
    }
}

int student(int index1){
    int c1,c2,c3,i,choice;
    while(1){
        l1:
        cout<<"choose an action to be performed:"<<endl;
        cout<<"1)book a room\n2)change room\n3)check status\n4)vacate room\n5)log out\n";
        cin>>c1;
        switch(c1){
            case 1:
                book(index1);
                break;
                
            case 2:
                change(index1);
                break;
                
            case 3:
                status(index1);
                if(s[index1].sharing!="single sharing" && s[index1].room!=NULL){
                    cout<<"show roomate details?"<<endl<<"1)YES\n2)NO\n";
                    cin>>choice;
                    if(choice==1){
                        roomate_details(index1);
                    }
                }
                break;
                
            case 4:
                vacate(index1);
                break;
                
            case 5:
                return 0;
                break;
                
            default:
                cout<<"invalid option\nchoose again\n";
                goto l1;
        }
    }
    return 0;
}

int warden_update(){
    int choice;
    string name;
    l13:
    cout<<"choose an action to be performed:"<<endl;
    cout<<"1)update wardens\n2)update warden's salary\n3)quit";
    cin>>choice;
    switch(choice){
        case 1:
            cout<<"enter warden name to be changed:"<<endl;
            cin>>name;
            if(gwarden==name){
                cout<<"enter new warden name:"<<endl;
                cin>>gwarden;
                cout<<"warden successfully changed!"<<endl;
            }
            else if(jwarden==name){
                cout<<"enter new warden name:"<<endl;
                cin>>jwarden;
                cout<<"warden successfully changed!"<<endl;
            }
            else if(ywarden==name){
                cout<<"enter new warden name:"<<endl;
                cin>>ywarden;
                cout<<"warden successfully changed!"<<endl;
            }
            else{
                cout<<"no match found please try again"<<endl;
                goto l13;
            }
            break;
        case 2:
            cout<<"enter warden name who's salary need to be changed:"<<endl;
            cin>>name;
            if(gwarden==name){
                cout<<"enter new salary:"<<endl;
                cin>>gsalary;
                cout<<"warden successfully changed!"<<endl;
            }
            else if(jwarden==name){
                cout<<"enter new salary:"<<endl;
                cin>>jsalary;
                cout<<"warden successfully changed!"<<endl;
            }
            else if(ywarden==name){
                cout<<"enter new salary:"<<endl;
                cin>>ysalary;
                cout<<"warden successfully changed!"<<endl;
            }
            else{
                cout<<"no match found please try again"<<endl;
                goto l13;
            }
            break;
            
        case 3:
            return 0;
            
        default:
            cout<<"invalid choice\nplease choose again:"<<endl;
            goto l13;
    }
}

int incharge2(int sn){
    int choice,i,flag=1,choice2;
    string adn,dob;
    while(1){
        cout<<"choose an action to be performed:"<<endl;
        cout<<"1)update student details\n2)details of a particular student\n3)update staff details\n4)check vacancies\n5)display hostel details\n6)quit"<<endl;
        cin>>choice;
        switch(choice){
            case 1:
                cout<<"enter the admission number of the student:"<<endl;
                cin>>adn;
                l11:
                cout<<"enter the date of birth of the student(DD/MM/YYYY):"<<endl;
                cin>>dob;
                for(i=0;i<sn;i++){
                    if(s[i].adn==adn){
                        flag=0;
                        if(s[i].dob==dob){
                            student(i);
                            break;
                        }
                        else{
                            cout<<"incorrect date of birth,please try again"<<endl;
                            goto l11;
                        }
                    }
                }
                if(flag){
                    cout<<"no student with entered details are found!"<<endl;
                }
                break;
            
            case 2:
                cout<<"enter the admission number of the student:"<<endl;
                cin>>adn;
                l12:
                cout<<"enter the date of birth of the student(DD/MM/YYYY):"<<endl;
                cin>>dob;
                for(i=0;i<sn;i++){
                    if(s[i].adn==adn){
                        flag=0;
                        if(s[i].dob==dob){
                            status(i);
                            break;
                        }
                        else{
                            cout<<"incorrect date of birth,please try again"<<endl;
                            goto l12;
                        }
                    }
                }
                if(flag){
                    cout<<"no student with entered details are found!"<<endl;
                }
                break;
                
            case 3:
                cout<<"wardens of each hostel"<<endl;
                cout<<"GANGA :\nNAME-"<<gwarden<<"\nsalary-"<<gsalary<<endl;
                cout<<"JAMUNA :\nNAME-"<<jwarden<<"\nsalary-"<<jsalary<<endl;
                cout<<"YAMUNA :\nNAME-"<<ywarden<<"\nsalary-"<<ysalary<<endl;
                warden_update();
                break;
            
            case 4:
                cout<<"GANGA:"<<endl;
                int i,j,k,flag;
                for(i=0;i<5;i++){
                    if(i%2==0) cout<<"A/C"<<endl;
                    else cout<<"NON A/C"<<endl;
                    flag=0;
                    for(j=0;j<10;j++){
                        if(g[i][j].n1[0].check==NULL){
                                cout<<((i+1)*100)+(j+1)<<"  ";
                        }
                    }
                    cout<<endl;
                }
                
                cout<<"JAMUNA:"<<endl;
                for(i=0;i<5;i++){
                    if(i%2==0) cout<<"A/C"<<endl;
                    else cout<<"NON A/C"<<endl;
                    flag=0;
                    for(j=0;j<10;j++){
                        for(k=0;k<2;k++){
                            if(J[i][j].n2[k].check==NULL){
                                    cout<<((i+1)*100)+(j+1)<<"  ";
                                    break;
                            }
                        }
                    }
                    cout<<endl;
                }
                
                cout<<"YAMUNA:"<<endl;
                for(i=0;i<5;i++){
                    if(i%2==0) cout<<"A/C"<<endl;
                    else cout<<"NON A/C"<<endl;
                    flag=0;
                    for(j=0;j<10;j++){
                        for(k=0;k<3;k++){
                            if(y[i][j].n3[k].check==NULL){
                                    cout<<((i+1)*100)+(j+1)<<"  ";
                                    break;
                            }
                        }
                    }
                    cout<<endl;
                }
                break;
                
            case 5:
                l14:
                cout<<"choose the hostel:"<<endl;
                cout<<"1)GANGA\n2)JAMUNA\n3)YAMUNA"<<endl;
                cin>>choice2;
                switch(choice2){
                    case 1:
                        cout<<"GANGA:"<<endl;
                        for(i=0;i<sn;i++){
                            if(s[i].hname=="GANGA")
                                status(i);
                        }
                        break;
                    case 2:
                        cout<<"JAMUNA:"<<endl;
                        for(i=0;i<sn;i++){
                            if(s[i].hname=="JAMUNA")
                                status(i);
                        }
                        break;
                    case 3:
                        cout<<"YAMUNA:"<<endl;
                        for(i=0;i<sn;i++){
                            if(s[i].hname=="YAMUNA")
                                status(i);
                        }
                        break;
                    default:
                        cout<<"invalid choice, please choose again:"<<endl;
                        goto l14;
                }
                break;
                
            case 6:
                return 0;
                break;
            
            default:
                cout<<"invalid option, please choose again:"<<endl;
        }
    }
}

void incharge(int sn){
    string id,pass,id1="AP116",pass1="AP116";
    l9:
    cout<<"enter your employee id:"<<endl;
    cin>>id;
    if(id==id1){
        l10:
        cout<<"enter your password:"<<endl;
        cin>>pass;
        if(pass==pass1){
            incharge2(sn);
        }
        else{
            cout<<"incorrect password"<<endl;
            goto l10;
        }
    }
    else{
        cout<<"incorrect employee ID"<<endl;
        goto l9;
    }
}

int main() {
    int choice,flag,index1,sn,i;
    string name,adn,dob;
    gwarden="ramarao";
    jwarden="charan";
    ywarden="kalyan";
    gsalary=10000;
    jsalary=15000;
    ysalary=20000;
    sn=-1;
    cout<<"WELCOME TO SRM HOSTEL SERVICES"<<endl;
    while(1){
        flag=0;
        l8:
        cout<<"\nchoose your category:"<<endl;
        cout<<"1)student\n2)incharge\n3)quit\n";
        cin>>choice;
        switch(choice){
            case 1:
                cout<<"enter your admission number:"<<endl;
                cin>>adn;
                cout<<"enter our date of birth(DD/MM/YYYY):"<<endl;
                cin>>dob;
                for(i=0;i<=sn;i++){
                    if (s[i].adn==adn){
                        if(s[i].dob==dob){
                            index1=i;
                            flag=1;
                        }
                        else{
                            cout<<"incorrect credentials\n";
                            goto l8;
                        }
                    }
                }
                if(!flag){
                    sn++;
                    cout<<"please enter your name:"<<endl;
                    cin>>s[sn].name;
                    s[sn].adn=adn;
                    s[sn].dob=dob;
                    index1=sn;
                    student(index1);
                }
                else{
                    student(index1);
                }
                break;
            
            case 2:
                incharge(sn+1);
                break;
            case 3:
                cout<<"thank you!";
                return 0;
                
            default:
                cout<<"invalid option!!\nplease enter a valid option";
        }
    }
    
    return 0;
}
