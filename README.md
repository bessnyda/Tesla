#Tesla

    import static Projects.tesla.ChangePower.dobavitPOWER;
    import static Projects.tesla.ChangePower.zabratPOWER;

    enum ChangePower{
        dobavitPOWER, zabratPOWER
    }

    public class Tesla{
    private int GodVipuska=2010,Bagajnik_litrov=470, NadytihKoles=4, ZerkalSkameroy=0, HorsePower=320, NewtonMeters=450;
    private double RazgonDo100=3.5,RazhodElectroDvigatelyaLitrovNa100=7.9;
    private boolean RekyperativnoeTormojenie=false;
    private boolean Used= false;
    private final String Model_tesla = "Model 3";
    private boolean Nalichie=true;
    private int Iznos=5;
    
    private Tesla(int godVipuska, int Bagajnik_litrov,int NadytihKoles, int ZerkalSkameroy, boolean RekyperativnoeTormojenie, int HorsePower, int  NewtonMeters, boolean Used) {
        this.GodVipuska = godVipuska;
        this.Bagajnik_litrov = Bagajnik_litrov;
        this.NadytihKoles = NadytihKoles;
        this.ZerkalSkameroy = ZerkalSkameroy;
        this.HorsePower = HorsePower;
        this.NewtonMeters = NewtonMeters;
        this.Used = Used;
        this.RekyperativnoeTormojenie = RekyperativnoeTormojenie;
    }
    
        private final void ChangeHoursePower(ChangePower changesPower, int numberChanges) throws Exception {
        if(Nalichie==true){
            if (Iznos!=0) {
                if (numberChanges <= 650 && numberChanges >= 20) {
                    if (changesPower == dobavitPOWER) {

                        System.out.println("Изменения в машине = " + (HorsePower += numberChanges) + " (Тюнинг)");
                    } else {}
                    if (changesPower == zabratPOWER) {
                        System.out.println("Изменения в машине = " + (HorsePower -= numberChanges) + " (Тюнинг)");
                    } else {}

                    if (Iznos != 0) {
                        Iznos--;
                        System.out.println("Смотря на действия в машине, бил винесен износ и -5HP [" + (HorsePower - 5) + "]");
                    } else {}

                }else {
                    System.out.println("Ви ввели неправильное число распредиления мощности");}

                } else {
                    System.out.println("Машина не пригодна к езде! = Изношенность 100%");
                    throw new Exception();}

        }else {
            System.out.println("Машина не найдена.");
            throw new Exception();}

    }
        private final void CheckHoursePower() throws Exception {
            if(Nalichie==true){
            System.out.println("HoursePower: " + this.HorsePower);
            }else {
                System.out.println("Машина не найдена.");
                throw new Exception();
            }
        }

        private final void ChangeNewtonMeters(ChangePower changesPower, int numberChanges) throws Exception {
            if(Nalichie==true){
                if (Iznos!=0){
                    if (numberChanges <= 650 && numberChanges >= 20) {
                    if (changesPower==dobavitPOWER){
            System.out.println("Изменения в машине = " + (NewtonMeters+=numberChanges) + " (Тюнинг)");

        }else {}
                    if (changesPower==zabratPOWER){
            System.out.println("Изменения в машине = " + (NewtonMeters-=numberChanges) + " (Тюнинг)");
                    }else {}

            if (Iznos!=0){
                Iznos--;
                System.out.println("Смотря на действия в машине, бил винесен износ и -5NM ["+(NewtonMeters-5)+"]" );

                    }else {}
                    }else {
                        System.out.println("Ви ввели неправильное число распредиления мощности");}
                }else {
                System.out.println("Машина не пригодна к езде и изминениям! = Изношенность 100%");
                throw new Exception();}

            }else {
                System.out.println("Машина не найдена.");
                throw new Exception();
            }

    }
        private final void CheckNewtonMeters() throws Exception {
            if(Nalichie==true){
        System.out.println("NewtonMeters: " + this.NewtonMeters);
            }else {
                System.out.println("Машина не найдена.");
                throw new Exception();
            }
    }

        private final void IzbavitsaOtTesli() throws Exception {
            if(Nalichie==true) {
                this.Nalichie = false;
            }else {
                System.out.println("Машина не найдена.");
                throw new Exception();
            }
    }
        private final void PosmotretNalichieTesli() throws InterruptedException {
            System.out.println("Proizvoditsa proverka na Nalichie Tesla");
            Thread.sleep(3000);
       if (this.Nalichie==true){
           System.out.println("Nalichie Tesli podtverjdenno! Eto:  "+ Model_tesla + " ("+ GodVipuska+")");
       }else {
           System.out.println("Otsytstvie Tesli podtverjdenno!");
       }
    }

        private final void TuningRekyperativnoeTormojenie(boolean RekyperativnoeTormojenie) throws Exception {
            if(Nalichie==true){
                if (Iznos!=0){

                    if (RekyperativnoeTormojenie==false){
                        this.RekyperativnoeTormojenie=true;
                    } else {
                        this.RekyperativnoeTormojenie=false;
                    }if (Iznos!=0){
                        Iznos--;
                        System.out.println("Смотря на действия в машине, бил винесен износ." );

                    }else {}



                         }else {
                        System.out.println("Машина не пригодна к езде и изминениям! = Изношенность 100%");
                        throw new Exception();}

            }else {
                System.out.println("Машина не найдена.");
                throw new Exception();
            }

    }
        private final void PosmotretNalichieRekyperativnogoTormojeniya() throws Exception {
            if(Nalichie==true) {
            System.out.println("Proizvoditsa proverka RekyperativnogoTormojeniya");
            Thread.sleep(3000);
            if (this.RekyperativnoeTormojenie==true){
                System.out.println("Nalichie RekyperativnogoTormojeniya podtverjdenno!");
            }else {
                System.out.println("Otsytstvie RekyperativnogoTormojeniya Opravergnenno!");
            }}else {
                System.out.println("Машина не найдена.");
                throw new Exception();
            }
        }

        private final void ViehadVLes() throws Exception {
            if(Nalichie==true) {
            System.out.println("Ви с вашей машиной отправились в путешествие на тесле");
            Thread.sleep(4000);
            int a = (int) (Math.random()*(1+1)) +2;
            if (a==2){
                System.out.println("Ви переехали ветку и повредили колеса. Визиваем евакуатор");
                int b = (int) (Math.random()*(1+1)) +1;
                System.out.println("Ви повредили колес: "+b);
                NadytihKoles=NadytihKoles-b;
            }else {
                System.out.println("Все прошло успешно. Возращаемся домой.");
            }
            }else {
                System.out.println("Машина не найдена.");
                throw new Exception();
            }
        }
        private final void ZamenaKoles() throws Exception {
            if(Nalichie==true) {
            if (NadytihKoles==4){
                System.out.println("Замена колес не требуется! Все целие");

            }else if (NadytihKoles==0){
                System.out.println("Требуется замена 4 колес");
                Thread.sleep(4000);
                System.out.println("Колеса успешно заменени. Удачной дороги!");

            }else if (NadytihKoles==1){
                System.out.println("Требуется замена 3 колес");
                Thread.sleep(3000);
                System.out.println("Колеса успешно заменени. Удачной дороги!");

            }else if (NadytihKoles==2){
                System.out.println("Требуется замена 2 колес");
                Thread.sleep(2000);
                System.out.println("Колеса успешно заменени. Удачной дороги!");

            }else if (NadytihKoles==3){
                System.out.println("Требуется замена 1 колеса");
                Thread.sleep(1000);
                System.out.println("Колесо успешно заменено. Удачной дороги!");
        }
            }else {
                System.out.println("Машина не найдена.");
                throw new Exception();
            }
    }

        static void _otstyp(){
            System.out.println("**+/-/-/-/-/-/-/-/-/-/-/-/-/-/-/-/-/-/-/-/-/-/-/+**");
        }

    @Override
    public String toString() {
        return "Tesla{ " +
                "GodVipuska= " + GodVipuska +
                ", Bagajnik_litrov= " + Bagajnik_litrov +
                ", NadytihKoles= " + NadytihKoles +
                ", ZerkalSkameroy= " + ZerkalSkameroy +
                ", HorsePower= " + HorsePower +
                ", NewtonMeters= " + NewtonMeters +
                ", RazgonDo100= " + RazgonDo100 +
                ", RazhodElectroDvigatelyaLitrovNa100= " + RazhodElectroDvigatelyaLitrovNa100 +
                ", RekyperativnoeTormojenie= " + RekyperativnoeTormojenie +
                ", Used= " + Used +
                ", Model_tesla= '" + Model_tesla + '\'' +
                ", Nalichie= " + Nalichie +
                ", Iznos= " + Iznos +
                '}'+".";
    }

    public static void main(String[] args) throws Exception {
        Tesla Tesla = new Tesla(2022,600,4,2,true,420,470,true);
        Tesla.PosmotretNalichieTesli();
        System.out.println(Tesla);
        _otstyp();
        Tesla.PosmotretNalichieTesli();
        Tesla.PosmotretNalichieRekyperativnogoTormojeniya();
         _otstyp();
        Tesla.TuningRekyperativnoeTormojenie(!Tesla.RekyperativnoeTormojenie);
         _otstyp();
        Tesla.ViehadVLes();
         _otstyp();
        Tesla.ZamenaKoles();
         _otstyp();
        Tesla.CheckHoursePower();
         _otstyp();
        Tesla.ChangeHoursePower(dobavitPOWER,200);
        Tesla.CheckHoursePower();
         _otstyp();
        Tesla.ChangeHoursePower(zabratPOWER,200);
         _otstyp();
        Tesla.CheckHoursePower();
         _otstyp();
        Tesla.CheckNewtonMeters();
         _otstyp();
        Tesla.ChangeNewtonMeters(dobavitPOWER,365);
         _otstyp();
        Tesla.CheckNewtonMeters();
         _otstyp();
        Tesla.ChangeNewtonMeters(zabratPOWER,365);
         _otstyp();
        Tesla.CheckNewtonMeters();
         _otstyp();
        Tesla.PosmotretNalichieTesli();
        _otstyp();
        Tesla.IzbavitsaOtTesli();
        _otstyp();
        Tesla.PosmotretNalichieTesli();
        Tesla.ChangeNewtonMeters(zabratPOWER,365);
    }
}
