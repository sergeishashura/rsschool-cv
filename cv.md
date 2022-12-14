1.Sergei Shashura
2.tg @shashuraz
3.I am a first-year student of the Belarusian University of Belarusian State University (Faculty of Radiophysics and Computer Technologies). I have always been interested in the topic of IT, in the early classes I was preparing for the Olympiads on Pascal.ABC. I want to create convenient services for people and work on interesting projects, and that is why I started my studies at RS in order to gain knowledge and experience for further work.
4.I am currently studying C++ at my university.
5.code example:
#include <iostream>
using namespace std;
enum ARRAY_USER_INPUT
{
    WORK_WITH_DEFAULT_ARRAY = 1,
    WORK_WITH_RANDOM_MEMBERS,
    WORK_WITH_USER_INPUT,
};
void fill_with_ready_array(const int amount, int array[], const int default_array[])
{
    cout << "default array = ";
    for (int i = 0; i < amount; i++)
    {
        array[i] = default_array[i];
    }
}
void fill_with_random_array(const int amount, int array[])
{
    cout << "random array = ";
    for (int element_array = 0; element_array < amount; element_array++)
    {
        array[element_array] = 1 + rand() % 9;
        cout << array[element_array] << " ";
    }
    cout << endl;
}
void fill_with_user_input(const int amount, int array[])
{
    cout << "enter number of array : " << endl;
    for (int element_array = 0; element_array < amount; element_array++)
    {
        cout << "[" << element_array << "]"
             << ":";
        cin >> array[element_array];
    }
}
int calculate_number_of_invertions(int amount, int array[], int number_of_inversions)
{
    for (int element_array = 0; element_array < amount - 1; element_array++)
    {
        if (array[element_array] > array[element_array + 1])
        {
            number_of_inversions++;
        }
    }
    return number_of_inversions;
}
int main()
{
    int num_way, number_of_inversions = 0;
    const int amount = 5;
    const int default_array[amount] = {5, 1, 3, 3, 5};
    int array[amount];
    cout << "number elements of array = 5 " << endl;
    cout << "select the way of fulfillment:" << endl;
    cout << "enter '1' if you want work with ready array;" << endl;
    cout << "enter '2' if you want work with random members of array;" << endl;
    cout << "enter '3' and members of array if you to want work with array;" << endl;
    cout << "enter number of your choice: ";
    cin >> num_way;

    switch (num_way)
    {
    case WORK_WITH_DEFAULT_ARRAY:
        fill_with_ready_array(amount, array, default_array);
        break;
    case WORK_WITH_RANDOM_MEMBERS:
        srand(time(0));
        fill_with_random_array(amount, array);
        break;
    case WORK_WITH_USER_INPUT:
        fill_with_user_input(amount, array);
        break;
    default:
        cout << "ERROR" << endl;
    }
    cout << "number of inversions = " << calculate_number_of_invertions(amount, array, number_of_inversions);
}
7. I didn't take any courses
8.English level approximately B1. I gained experience of communication on it when talking with my teacher. She really liked talking to me, and since at that time I had an extremely poor command of it, we discussed everyday things, music, movies and news several times a day.
