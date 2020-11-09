---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296872"
---
# Backup-AzManagedHsmKey

## Synopsis
Sichern eines Schlüssels in einem verwalteten HSM

## Syntax

### ByKeyName (Standard)
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Backup-AzManagedHsmKey** sichern einen angegebenen Schlüssel in einem verwalteten HSM, indem Sie es herunterladen und in einer Datei speichern.
Wenn mehrere Versionen des Schlüssels vorhanden sind, werden alle Versionen in die Sicherung aufgenommen.
Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb von Azure Managed HSM verwendet werden.
Sie können einen gesicherten Schlüssel für ein verwaltetes HSM im Abonnement wiederherstellen, von dem es gesichert wurde.
Typische Gründe für die Verwendung dieses Cmdlets sind: 
- Sie möchten eine Kopie Ihres Schlüssels hinterlegen, damit Sie eine Offlinekopie haben, falls Sie Ihren Schlüssel versehentlich in Ihrem Managed HSM löschen.
 
- Sie haben einen Schlüssel mit verwaltetem HSM erstellt und möchten nun den Schlüssel in einen anderen Azure-Bereich Klonen, sodass Sie ihn aus allen Instanzen ihrer verteilten Anwendung verwenden können.
Verwenden Sie das Cmdlet **Backup-AzManagedHsmKey** , um den Schlüssel im verschlüsselten Format abzurufen, und verwenden Sie dann das Restore-AzManagedHsmKey-Cmdlet, und geben Sie im zweiten Bereich ein verwaltetes HSM an.

## Beispiele

### Beispiel 1: Sichern eines Schlüssels mit einem automatisch generierten Dateinamen
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

Dieser Befehl ruft den Schlüssel mit dem Namen TestKey aus dem verwalteten HSM mit dem Namen testmhsm ab und speichert eine Sicherungskopie dieses Schlüssels in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Überschreiben der angegebenen Datei, sofern vorhanden

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmName
HSM-Name. Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Schlüsselpaket, das von der Ausgabe eines Abruf Anrufs in eine Sicherungskopie geleitet wird.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Schlüsselname.
Cmdlet erstellt den FQDN eines Schlüssels aus verwaltetem HSM-Namen, aktuell ausgewählter Umgebung und Schlüsselname.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Outputdatei
Ausgabedatei.
Die Ausgabedatei, in der der gesicherte Schlüssel BLOB gespeichert werden soll.
Wenn diese nicht vorhanden ist, wird ein Standarddateiname ausgewählt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem

## Ausgaben

### System. String

## Notizen

## Verwandte Links

[Add-AzManagedHsmKey](./Add-AzManagedHsmKey.md)

[Get-AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[Remove-AzManagedHsmKey](./Remove-AzManagedHsmKey.md)

[Undo-AzManagedHsmKeyRemoval](./Undo-AzManagedHsmKeyRemoval.md)

[Update-AzManagedHsmKey](./Update-AzManagedHsmKey.md)

[Wiederherstellen – AzManagedHsmKey](./Restore-AzManagedHsmKey.md)