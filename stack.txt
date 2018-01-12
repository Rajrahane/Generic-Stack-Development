#include<iostream.h>

template<class T>
class Stack{
	private:
		T stk[10];
		int stk_ptr;
	public:
		Stack(){
			stk_ptr=-1;
		}
		void push(T element){
			if(stk_ptr==9)
				cout<<"Stack Full\n";
			else{
				stk_ptr++;
				stk[stk_ptr]=element;
			}	
		}
		T pop(){
			if(stk_ptr==-1){
				cout<<"Stack Empty\n";
				return -1;
			}
			else{
				T element;
				element=stk[stk_ptr--];
				return element;
			}
		} 

};


void main(){

	Stack<int> newStk;
	newStk.push(5);
	cout<<newStk.pop();

}