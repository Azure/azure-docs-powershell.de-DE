---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010056"
---
# Set-AzAutomationCredential

## Synopsis
Ändert eine Automatisierungs Anmeldeinformationen.

## Syntax

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzAutomationCredential** " ändert eine Anmeldeinformationen als **PSCredential** -Objekt in Azure-Automatisierung.

## Beispiele

### Beispiel 1: Aktualisieren von Anmeldeinformationen
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

Der erste Befehl weist der $User-Variablen einen Benutzernamen zu.
Mit dem zweiten Befehl wird ein nur-Text-Kennwort mithilfe des ConvertTo-SecureString-Cmdlets in eine sichere Zeichenfolge konvertiert.
Der Befehl speichert das Objekt in der $Password Variablen.
Der dritte Befehl erstellt eine Anmeldeinformationen basierend auf $User und $Password und speichert Sie dann in der $Credential-Variablen.
Der endgültige Befehl ändert die Automatisierungs Anmeldeinformationen mit dem Namen ContosoCredential, um die Anmeldeinformationen in $Credential zu verwenden.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, für das mit diesem Cmdlet eine Anmeldeinformation geändert wird.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Gibt eine Beschreibung für die Anmeldeinformationen an, die von diesem Cmdlet geändert werden.

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

### -Name
Gibt den Namen der Anmeldeinformationen an, die von diesem Cmdlet geändert werden.

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
Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Anmeldeinformationen ändert.

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

### -Wert
Gibt die Anmeldeinformationen als **PSCredential** -Objekt an.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. Management. Automation. PSCredential

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. CredentialInfo

## Notizen

## Verwandte Links

[Get-AzAutomationCredential](./Get-AzAutomationCredential.md)

[Neu – AzAutomationCredential](./New-AzAutomationCredential.md)

[Remove-AzAutomationCredential](./Remove-AzAutomationCredential.md)


