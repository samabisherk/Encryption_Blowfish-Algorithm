package Cryptography;
 
import javax.crypto.Cipher;
import javax.crypto.spec.SecretKeySpec;
import sun.misc.BASE64Decoder;
import sun.misc.BASE64Encoder;
 
public class BlowfishAlgorithm {
 
    public static void main(String[] args) throws Exception {

        encrypt("abisherk","pass123");
        decrypt("d4HNr5wB/C4=");
    }

    private static void encrypt(String username, String password) throws Exception {
        byte[] keyData = (username+password).getBytes();
        SecretKeySpec Key= new SecretKeySpec(keyData, "Blowfish");
        Cipher encryptionMethod = Cipher.getInstance("Blowfish");
        encryptionMethod.init(Cipher.ENCRYPT_MODE, Key);
        byte[] EncryptedValue= encryptionMethod.doFinal(password.getBytes());
        System.out.println("Encrypted Value:" + EncryptedValue);
        System.out.println("Encoded Value:" + new BASE64Encoder().encode(EncryptedValue));
    }

    private static void decrypt(String string) throws Exception {

        byte[] keyData = ("abisherk"+"pass123").getBytes();
        SecretKeySpec secretKeySpec = new SecretKeySpec(keyData, "Blowfish");
        Cipher decryptionMethod = Cipher.getInstance("Blowfish");
        decryptionMethod.init(Cipher.DECRYPT_MODE, secretKeySpec);
        byte[] DecryptedValue = decryptionMethod.doFinal(new BASE64Decoder().decodeBuffer(string));
        System.out.println("Decrypted Value:" + new String(DecryptedValue));
    }
}

