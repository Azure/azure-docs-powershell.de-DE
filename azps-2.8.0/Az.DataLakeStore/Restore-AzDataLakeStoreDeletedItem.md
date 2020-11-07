---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 7df59f75200bbc0d52c595c263228d7bf9801486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651511"
---
# <span data-ttu-id="ad1a9-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="ad1a9-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="ad1a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1a9-103">Wiederherstellen einer gelöschten Datei oder eines gelöschten Ordners in Azure Data Lake</span><span class="sxs-lookup"><span data-stu-id="ad1a9-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="ad1a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad1a9-104">SYNTAX</span></span>

### <span data-ttu-id="ad1a9-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad1a9-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad1a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ad1a9-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad1a9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad1a9-107">DESCRIPTION</span></span>
<span data-ttu-id="ad1a9-108">Das Cmdlet **Restore-AzDataLakeStoreDeletedItem** stellt eine gelöschte Datei oder einen gelöschten Ordner im Data Lake Store wieder her.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="ad1a9-109">Erfordert den Pfad des gelöschten Elements im Papierkorb, der von Get-AzDataLakeStoreDeletedItem zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="ad1a9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad1a9-110">EXAMPLES</span></span>

### <span data-ttu-id="ad1a9-111">Beispiel 1: Wiederherstellen einer Datei aus der Data Lake Store-Option mit Kraft</span><span class="sxs-lookup"><span data-stu-id="ad1a9-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="ad1a9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad1a9-112">PARAMETERS</span></span>

### <span data-ttu-id="ad1a9-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="ad1a9-113">-Account</span></span>
<span data-ttu-id="ad1a9-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ad1a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1a9-115">-DefaultProfile</span></span>
<span data-ttu-id="ad1a9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad1a9-117">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="ad1a9-117">-DeletedItem</span></span>
<span data-ttu-id="ad1a9-118">Das gelöschte Element-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-118">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1a9-119">-Ziel</span><span class="sxs-lookup"><span data-stu-id="ad1a9-119">-Destination</span></span>
<span data-ttu-id="ad1a9-120">Der Zielpfad, in dem die gelöschte Datei oder der gelöschte Ordner wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-120">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1a9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ad1a9-121">-Force</span></span>
<span data-ttu-id="ad1a9-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad1a9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad1a9-123">-PassThru</span></span>
<span data-ttu-id="ad1a9-124">Geben Sie beim Erfolg boolescher Wert true zurück.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-124">Return boolean true on success.</span></span>

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

### <span data-ttu-id="ad1a9-125">-Path</span><span class="sxs-lookup"><span data-stu-id="ad1a9-125">-Path</span></span>
<span data-ttu-id="ad1a9-126">Der Pfad der gelöschten Datei oder des gelöschten Ordners im Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-126">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1a9-127">-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="ad1a9-127">-RestoreAction</span></span>
<span data-ttu-id="ad1a9-128">Aktion zur übernehmen von Ziel Namenskonflikten – "Kopieren" oder "überschreiben"</span><span class="sxs-lookup"><span data-stu-id="ad1a9-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="ad1a9-129">-Typ</span><span class="sxs-lookup"><span data-stu-id="ad1a9-129">-Type</span></span>
<span data-ttu-id="ad1a9-130">Der Typ des wiederherzustellenden Eintrags-"Datei" oder "Ordner"</span><span class="sxs-lookup"><span data-stu-id="ad1a9-130">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1a9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1a9-131">CommonParameters</span></span>
<span data-ttu-id="ad1a9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad1a9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1a9-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad1a9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1a9-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad1a9-134">INPUTS</span></span>

### <span data-ttu-id="ad1a9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ad1a9-135">System.String</span></span>

## <span data-ttu-id="ad1a9-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad1a9-136">OUTPUTS</span></span>

### <span data-ttu-id="ad1a9-137">Keine</span><span class="sxs-lookup"><span data-stu-id="ad1a9-137">None</span></span>

## <span data-ttu-id="ad1a9-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad1a9-138">NOTES</span></span>

## <span data-ttu-id="ad1a9-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad1a9-139">RELATED LINKS</span></span>

[<span data-ttu-id="ad1a9-140">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="ad1a9-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)