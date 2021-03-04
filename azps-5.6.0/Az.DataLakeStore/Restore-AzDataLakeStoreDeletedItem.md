---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: ba8a97e96a07e63cd3b1f63c85a71291c59fdab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920728"
---
# <span data-ttu-id="5ba5d-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="5ba5d-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="5ba5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ba5d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba5d-103">Wiederherstellen einer gelöschten Datei oder eines gelöschten Ordners in Azure Data Lake</span><span class="sxs-lookup"><span data-stu-id="5ba5d-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="5ba5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ba5d-104">SYNTAX</span></span>

### <span data-ttu-id="5ba5d-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ba5d-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ba5d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5ba5d-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ba5d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ba5d-107">DESCRIPTION</span></span>
<span data-ttu-id="5ba5d-108">Mit **dem Cmdlet Restore-AzDataLakeStoreDeletedItem** wird eine gelöschte Datei oder ein gelöschter Ordner im Data Lake Store wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="5ba5d-109">Erfordert den Pfad des gelöschten Elements im Papierkorb, der von Get-AzDataLakeStoreDeletedItem zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="5ba5d-110">Vorsicht: Das Rückgängig machen von Dateien ist ein Vorgang am besten.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="5ba5d-111">Es gibt keine Garantien dafür, dass eine Datei nach dem Löschen wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="5ba5d-112">Die Verwendung dieser API wird über whitelisting aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="5ba5d-113">Wenn Ihr ADL-Konto nicht auf der Whitelist aufgeführt ist, wird mit dieser Api die Ausnahme Nicht implementiert ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="5ba5d-114">Weitere Informationen und Unterstützung erhalten Sie vom Microsoft-Support.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="5ba5d-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ba5d-115">EXAMPLES</span></span>

### <span data-ttu-id="5ba5d-116">Beispiel 1: Wiederherstellen einer Datei aus dem Data Lake Store mithilfe der Option "-force"</span><span class="sxs-lookup"><span data-stu-id="5ba5d-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="5ba5d-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5ba5d-117">PARAMETERS</span></span>

### <span data-ttu-id="5ba5d-118">-Konto</span><span class="sxs-lookup"><span data-stu-id="5ba5d-118">-Account</span></span>
<span data-ttu-id="5ba5d-119">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5ba5d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba5d-120">-DefaultProfile</span></span>
<span data-ttu-id="5ba5d-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba5d-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="5ba5d-122">-DeletedItem</span></span>
<span data-ttu-id="5ba5d-123">Das gelöschte Elementobjekt.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-123">The deleted item object.</span></span>

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

### <span data-ttu-id="5ba5d-124">-Ziel</span><span class="sxs-lookup"><span data-stu-id="5ba5d-124">-Destination</span></span>
<span data-ttu-id="5ba5d-125">Der Zielpfad, zu dem die gelöschte Datei oder der gelöschte Ordner wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="5ba5d-126">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="5ba5d-126">-Force</span></span>
<span data-ttu-id="5ba5d-127">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ba5d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ba5d-128">-PassThru</span></span>
<span data-ttu-id="5ba5d-129">Geben Sie boolescher Wahr bei Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="5ba5d-130">-Path</span><span class="sxs-lookup"><span data-stu-id="5ba5d-130">-Path</span></span>
<span data-ttu-id="5ba5d-131">Der Pfad der gelöschten Datei oder des gelöschten Ordners im Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="5ba5d-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="5ba5d-132">-RestoreAction</span></span>
<span data-ttu-id="5ba5d-133">Aktion zum Ergreifen von Zielnamenkonflikten – "Kopieren" oder "Überschreiben"</span><span class="sxs-lookup"><span data-stu-id="5ba5d-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="5ba5d-134">-Type</span><span class="sxs-lookup"><span data-stu-id="5ba5d-134">-Type</span></span>
<span data-ttu-id="5ba5d-135">Der Typ des wiederhergestellten Eintrags – "Datei" oder "Ordner"</span><span class="sxs-lookup"><span data-stu-id="5ba5d-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="5ba5d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba5d-136">CommonParameters</span></span>
<span data-ttu-id="5ba5d-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba5d-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba5d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba5d-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ba5d-139">INPUTS</span></span>

### <span data-ttu-id="5ba5d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5ba5d-140">System.String</span></span>

## <span data-ttu-id="5ba5d-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ba5d-141">OUTPUTS</span></span>

### <span data-ttu-id="5ba5d-142">Keine</span><span class="sxs-lookup"><span data-stu-id="5ba5d-142">None</span></span>

## <span data-ttu-id="5ba5d-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5ba5d-143">NOTES</span></span>

## <span data-ttu-id="5ba5d-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5ba5d-144">RELATED LINKS</span></span>

[<span data-ttu-id="5ba5d-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="5ba5d-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)