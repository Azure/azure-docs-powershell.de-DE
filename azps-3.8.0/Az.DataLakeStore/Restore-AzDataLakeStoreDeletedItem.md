---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005243"
---
# <span data-ttu-id="b2fdb-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="b2fdb-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="b2fdb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="b2fdb-103">Wiederherstellen einer gelöschten Datei oder eines gelöschten Ordners in Azure Data Lake</span><span class="sxs-lookup"><span data-stu-id="b2fdb-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="b2fdb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2fdb-104">SYNTAX</span></span>

### <span data-ttu-id="b2fdb-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2fdb-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2fdb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b2fdb-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2fdb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2fdb-107">DESCRIPTION</span></span>
<span data-ttu-id="b2fdb-108">Das Cmdlet **Restore-AzDataLakeStoreDeletedItem** stellt eine gelöschte Datei oder einen gelöschten Ordner im Data Lake Store wieder her.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="b2fdb-109">Erfordert den Pfad des gelöschten Elements im Papierkorb, der von Get-AzDataLakeStoreDeletedItem zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="b2fdb-110">Vorsicht: beim Löschen von Dateien handelt es sich um eine optimale Aktion.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="b2fdb-111">Es gibt keine Garantien, dass eine Datei wiederhergestellt werden kann, nachdem Sie gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="b2fdb-112">Die Verwendung dieser API wird über die Whitelist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="b2fdb-113">Wenn Ihr ADL-Konto nicht in der Whitelist enthalten ist, löst die Verwendung dieser API keine implementierte Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="b2fdb-114">Wenn Sie weitere Informationen benötigen, wenden Sie sich bitte an den Microsoft-Support.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="b2fdb-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2fdb-115">EXAMPLES</span></span>

### <span data-ttu-id="b2fdb-116">Beispiel 1: Wiederherstellen einer Datei aus der Data Lake Store-Option mit Kraft</span><span class="sxs-lookup"><span data-stu-id="b2fdb-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="b2fdb-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2fdb-117">PARAMETERS</span></span>

### <span data-ttu-id="b2fdb-118">-Konto</span><span class="sxs-lookup"><span data-stu-id="b2fdb-118">-Account</span></span>
<span data-ttu-id="b2fdb-119">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b2fdb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2fdb-120">-DefaultProfile</span></span>
<span data-ttu-id="b2fdb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2fdb-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="b2fdb-122">-DeletedItem</span></span>
<span data-ttu-id="b2fdb-123">Das gelöschte Element-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-123">The deleted item object.</span></span>

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

### <span data-ttu-id="b2fdb-124">-Ziel</span><span class="sxs-lookup"><span data-stu-id="b2fdb-124">-Destination</span></span>
<span data-ttu-id="b2fdb-125">Der Zielpfad, in dem die gelöschte Datei oder der gelöschte Ordner wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="b2fdb-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b2fdb-126">-Force</span></span>
<span data-ttu-id="b2fdb-127">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b2fdb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2fdb-128">-PassThru</span></span>
<span data-ttu-id="b2fdb-129">Geben Sie beim Erfolg boolescher Wert true zurück.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="b2fdb-130">-Path</span><span class="sxs-lookup"><span data-stu-id="b2fdb-130">-Path</span></span>
<span data-ttu-id="b2fdb-131">Der Pfad der gelöschten Datei oder des gelöschten Ordners im Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="b2fdb-132">-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="b2fdb-132">-RestoreAction</span></span>
<span data-ttu-id="b2fdb-133">Aktion zur übernehmen von Ziel Namenskonflikten – "Kopieren" oder "überschreiben"</span><span class="sxs-lookup"><span data-stu-id="b2fdb-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="b2fdb-134">-Typ</span><span class="sxs-lookup"><span data-stu-id="b2fdb-134">-Type</span></span>
<span data-ttu-id="b2fdb-135">Der Typ des wiederherzustellenden Eintrags-"Datei" oder "Ordner"</span><span class="sxs-lookup"><span data-stu-id="b2fdb-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="b2fdb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2fdb-136">CommonParameters</span></span>
<span data-ttu-id="b2fdb-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2fdb-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2fdb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2fdb-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2fdb-139">INPUTS</span></span>

### <span data-ttu-id="b2fdb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b2fdb-140">System.String</span></span>

## <span data-ttu-id="b2fdb-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2fdb-141">OUTPUTS</span></span>

### <span data-ttu-id="b2fdb-142">Keine</span><span class="sxs-lookup"><span data-stu-id="b2fdb-142">None</span></span>

## <span data-ttu-id="b2fdb-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2fdb-143">NOTES</span></span>

## <span data-ttu-id="b2fdb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2fdb-144">RELATED LINKS</span></span>

[<span data-ttu-id="b2fdb-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="b2fdb-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)