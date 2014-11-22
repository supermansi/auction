import java.util.*;
import java.lang.*;
import java.io.*;
public class Auction
{
	public static void main(String args[])throws IOException
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter total number of players:");
		int n=sc.nextInt();
		System.out.println("Enter no. of teams:");
		int nt=sc.nextInt();
		int np=n-nt;
		int i,j;
		String a[][]=new String[n][4];
		System.out.println("Enter name and grade of captain:");
		for(i=0;i<nt;i++)
		{
		    for(j=0;j<2;j++)
		    {
		        a[i][j]=sc.next();  
		    }
		  }
		String b[]=new String[np];
		System.out.println("Enter Grade of remaining players:");
		for(i=0;i<np;i++)
		{	
			b[i]=sc.nextLine();
		}
		int na=0,nb=0,nc=0,nd=0;
		for(i=0;i<np;i++)
		{
			if(b[i].equals("A"))
			{
				na++;
			}
			else if(b[i].equals("B"))
			{
				nb++;
			}
			else if(b[i].equals("C"))
			{
				nc++;
			}
			else if(b[i].equals("D"))
			{
				nd++;
			}
		}
		int sum=40*na+30*nb+20*nc+10*nd;
		int[] n_p_t={9,9,9,9,9,9,9};
		int n_p_c[]=new int[7];
		for(i=0;i<7;i++)
		{
			if(a[i][1].equals("A"))
			{
				n_p_c[i]=400;
			}
			else
			{
				n_p_c[i]=440;
			}
		}
		int b_p_c[]=new int[7];
		int cpt_b;
		String grade;
		int no_pts;
		int avg=sum/np;
		for(i=0;i<7;i++)
		{
			if(a[i][1].equals("A"))
			{
				b_p_c[i]=400-avg*8;
			}
			else if(a[i][1].equals("B"))
			{
				b_p_c[i]=440-avg*8;
			}
		}
		while(np>0)
		{
			np--;
			cpt_b=sc.nextInt();
			grade=sc.nextLine();
			no_pts=sc.nextInt();			
			if(grade.equals("A"))
			{
				sum-=40;
			}
			else if(grade.equals("B"))
			{
				sum-=30;
			}
			else if(grade.equals("C"))
			{
				sum-=20;
			}
			else if(grade.equals("D"))
			{
				sum-=10;
			}
			avg=sum/np;
			n_p_t[cpt_b]--;
			for(i=0;i<7;i++)
			{
				b_p_c[i]=n_p_c[i]-(avg*(--n_p_t[i]));
				n_p_c[i]-=no_pts;
			}
			for(i=0;i<7;i++)
			{
				System.out.println(i+"\t Remaining Points=  "+n_p_c[i]+"\t Bidding Power=  "+b_p_c[i]);
			}
		}
		
	}
}
