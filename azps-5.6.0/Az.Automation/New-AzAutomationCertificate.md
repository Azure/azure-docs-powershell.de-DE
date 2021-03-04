---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 3f92ebfcb9b768788b0a9acd7a1e11ef766fd22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948067"
---
# New-AzAutomationCertificate

## SYNOPSIS
Erstellt ein Automatisierungszertifikat.

## SYNTAX

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzAutomationCertificate** erstellt ein Zertifikat in Azure Automation.
Stellen Sie den Pfad zu einer Zertifikatdatei zum Hochladen zur Verfügung.

## BEISPIELE

### Beispiel 1: Erstellen eines neuen Zertifikats
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

Mit dem ersten Befehl wird ein Nur-Text-Kennwort mithilfe des cmdlets ConvertTo-SecureString in eine sichere Zeichenfolge konvertiert.
Der Befehl speichert dieses Objekt in der $Password Variablen.
Der zweite Befehl erstellt ein Zertifikat mit dem Namen ContosoCertificate.
Der Befehl verwendet das kennwort, das in $Password.
Der Befehl gibt den Kontonamen und den Pfad der Datei an, die hochgeladen wird.

## PARAMETER

### -AutomationAccountName
Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet das Zertifikat speichert.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Beschreibung
Gibt eine Beschreibung für das Zertifikat an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Exportierbar
Gibt an, ob das Zertifikat exportiert werden kann.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen für das Zertifikat an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Password
Gibt das Kennwort für die Zertifikatdatei an.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den Pfad zu einer Skriptdatei an, die von diesem Cmdlet hochgeladen wird.
Bei der Datei kann es sich um eine CER- oder eine PFX-Datei.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat erstellt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### System.Security.SecureString

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.Automation.Model.CertificateInfo

## NOTIZEN

Dieser Befehl sollte auf einem Computer ausgeführt werden, von dem Sie administrator sind, sowie in einer erhöhten PowerShell-Sitzung. bevor das Zertifikat hochgeladen wird, verwendet dieses Cmdlet den lokalen X.509-Store, um den Fingerabdruck und den Schlüssel abzurufen. Wenn dieses Cmdlet außerhalb einer powerShell-Sitzung mit erhöhten Rechten ausgeführt wird, wird der Fehler "Zugriff verweigert" angezeigt.

## VERWANDTE LINKS

[Get-AzAutomationCertificate](./Get-AzAutomationCertificate.md)

[Remove-AzAutomationCertificate](./Remove-AzAutomationCertificate.md)

[Set-AzAutomationCertificate](./Set-AzAutomationCertificate.md)


