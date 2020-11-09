---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297909"
---
# Export-AzDataLakeStoreChildItemProperty

## Synopsis
Exportiert die Eigenschaften (Datenträgerverwendung und ACL) für die gesamte Struktur aus dem angegebenen Pfad in einen Ausgabepfad.

## Syntax

### GetDiskUsage
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### GetAllProperties
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GetAclDump
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Der **Export-AzDataLakeStoreChildItemProperty** wird verwendet, um die ADLS-Speicherplatznutzung oder/und die ACL-Nutzung für das angegebene Verzeichnis und dessen Unterverzeichnisse und Dateien zu melden.

## Beispiele

### Beispiel 1: Abrufen der Datenträgerverwendung und ACL-Verwendung für alle Unterverzeichnisse und Dateien
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

Abrufen der Datenträgerverwendung und ACL-Verwendung für alle Unterverzeichnisse und Dateien unter/a Include-Datei stellt sicher, dass die Verwendung auch für Dateien gemeldet wird

### Beispiel 2: Abrufen der ACL-Verwendung für alle Unterverzeichnisse und Dateien mit ausgeblendeter konsistenter ACL
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

Abrufen der ACL-Nutzung für alle Unterverzeichnisse und Dateien unter/a Include-Datei stellt sicher, dass die Verwendung auch für Dateien gemeldet wird. HideconsistentAcl in diesem Fall wird die ACL von/a angezeigt, nicht die Kinder, da alle untergeordneten Elemente dieselbe ACL wie/a Dieses Flag überspringt die ACL-Ausgabe der Teilstruktur, wenn alle ACLs identisch mit dem Stammverzeichnis sind.

## Parameter

### -Konto
Das Data Lake Store-Konto zum Ausführen des Dateisystem Vorgangs in

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parallelität
Gibt an, wie viele Dateien/Verzeichnisse parallel verarbeitet werden.
Der Standardwert wird basierend auf der Systemspezifikation als optimaler Aufwand berechnet.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -GetAcl
Ruft die ACL ab dem Stamm Pfad ab.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GetDiskUsage
Ruft die Datenträgernutzung ab, beginnend mit dem Stamm Pfad.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HideConsistentAcl
Directory-Unterstruktur nicht anzeigen, wenn die ACLs in der gesamten Unterstruktur identisch sind. Dadurch ist es einfacher, nur die Pfade anzuzeigen, nach denen sich die ACLs unterscheiden. Wenn beispielsweise alle Dateien und Ordner unter/a/b identisch sind, zeigen Sie die subtreeunder-/a/b nicht an, und geben Sie nur/a/b mit "true" in der konsistenten ACL-columnCannot ein, wenn IncludeFiles nicht festgelegt ist, da die konsistente ACL nicht ermittelt werden kann, ohne dass ACLs für die Dateien abgerufen werden.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Include-Datei
Stats auf Dateiebene anzeigen (Standardmäßig werden nur Informationen auf Verzeichnisebene angezeigt)

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

### -MaximumDepth
Maximale Tiefe aus dem Stammverzeichnis bis zur Anzeige der Datenträgernutzung oder ACL

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputPath
Pfad zur Ausgabedatei Kann ein lokaler Pfad oder ein ADL-Pfad sein. Standardmäßig ist es lokal. Wenn SaveToAdl angegeben ist, handelt es sich um einen ADL-Pfad im gleichen Konto.

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

### -PassThru
Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.

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

### -Path
Der Pfad im angegebenen Data Lake-Konto, das abgerufen werden soll.
Kann eine Datei oder ein Ordner im Format "/Folder/file.txt" sein, wobei der erste "/" nach dem DNS den Stamm des Dateisystems angibt.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SaveToAdl
Wenn übergeben, wird die Speicherabbilddatei in ADL gespeichert.
In diesem Fall ist die Dumpdatei ein ADL-Pfad.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance

### System. Management. Automation. Switchparameter

### System. Int32

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links
