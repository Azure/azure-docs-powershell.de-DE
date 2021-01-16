---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376268"
---
# Get-AzStorageAccountKey

## SYNOPSIS
Ruft die Zugriffstasten für ein Azure Storage-Konto ab.

## SYNTAX

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzStorageAccountKey"** ruft die Zugriffsschlüssel für ein Azure Storage-Konto ab.

## BEISPIELE

### Beispiel 1: Erhalten der Zugriffstasten für ein Speicherkonto
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

Dieser Befehl ruft die Schlüssel für das angegebene Azure Storage-Konto ab.

### Beispiel 2: Erhalten eines bestimmten Zugriffsschlüssels für ein Speicherkonto
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### Beispiel 3: Listet die Zugriffstasten für ein Speicherkonto auf, enthält die Kerberos-Schlüssel (wenn Active Directory aktiviert ist)
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

Dieser Befehl ruft die Schlüssel für das angegebene Azure Storage-Konto ab.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -ListKerbKey
Listet die Kerberos-Schlüssel (wenn Active Directory aktiviert ist) für das angegebene Speicherkonto auf.
Der Kerberos-Schlüssel wird pro Speicherkonto für die identitätsbasierte Authentifizierung in Azure Files entweder mit Azure Active Directory Domain Service (Azure AD DS) oder Active Directory Domain Service (AD DS) generiert. Es wird als Kennwort der Identität verwendet, die im Domänendienst registriert ist, der das Speicherkonto darstellt. Der Kerberos Key bietet keine Zugriffsberechtigungen zum Ausführen von Steuerelement- oder Datenebenen-Lese- oder -Schreibvorgängen für das Speicherkonto.

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

### -Name
Gibt den Namen des Speicherkontos an, für das dieses Cmdlet Schlüssel erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Management.Storage.Models.StorageAccountKey

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzStorageAccountKey](./New-AzStorageAccountKey.md)


