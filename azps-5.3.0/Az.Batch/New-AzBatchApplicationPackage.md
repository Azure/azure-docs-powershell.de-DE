---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471144"
---
# <span data-ttu-id="4df94-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4df94-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="4df94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df94-102">SYNOPSIS</span></span>
<span data-ttu-id="4df94-103">Erstellt ein Anwendungspaket in einem Batchkonto.</span><span class="sxs-lookup"><span data-stu-id="4df94-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="4df94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4df94-104">SYNTAX</span></span>

### <span data-ttu-id="4df94-105">UploadAndActivate (Standard)</span><span class="sxs-lookup"><span data-stu-id="4df94-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4df94-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="4df94-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4df94-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4df94-107">DESCRIPTION</span></span>
<span data-ttu-id="4df94-108">Das **Cmdlet "New-AzBatchApplicationPackage"** erstellt ein Anwendungspaket in einem Azure Batch-Konto.</span><span class="sxs-lookup"><span data-stu-id="4df94-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="4df94-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4df94-109">EXAMPLES</span></span>

### <span data-ttu-id="4df94-110">Beispiel 1: Installieren eines Anwendungspakets in einem Batchkonto</span><span class="sxs-lookup"><span data-stu-id="4df94-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="4df94-111">Dieser Befehl erstellt und aktiviert Version 1.0 der Litware-Anwendung und lädt den Inhalt des litware.1.0.zip als Anwendungspaketinhalt hoch.</span><span class="sxs-lookup"><span data-stu-id="4df94-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="4df94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4df94-112">PARAMETERS</span></span>

### <span data-ttu-id="4df94-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4df94-113">-AccountName</span></span>
<span data-ttu-id="4df94-114">Gibt den Namen des Batchkontos an, dem dieses Cmdlet ein Anwendungspaket hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="4df94-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="4df94-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="4df94-115">-ActivateOnly</span></span>
<span data-ttu-id="4df94-116">Gibt an, dass mit diesem Cmdlet ein Anwendungspaket aktiviert wird, das bereits hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="4df94-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df94-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="4df94-117">-ApplicationName</span></span>
<span data-ttu-id="4df94-118">Gibt den Namen der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="4df94-118">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df94-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="4df94-119">-ApplicationVersion</span></span>
<span data-ttu-id="4df94-120">Gibt die Version der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="4df94-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df94-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df94-121">-DefaultProfile</span></span>
<span data-ttu-id="4df94-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4df94-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df94-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="4df94-123">-FilePath</span></span>
<span data-ttu-id="4df94-124">Gibt die Datei an, die als Binärdatei des Anwendungspakets hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4df94-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df94-125">-Format</span><span class="sxs-lookup"><span data-stu-id="4df94-125">-Format</span></span>
<span data-ttu-id="4df94-126">Gibt das Format der Binärdatei des Anwendungspakets an.</span><span class="sxs-lookup"><span data-stu-id="4df94-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4df94-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df94-127">-ResourceGroupName</span></span>
<span data-ttu-id="4df94-128">Gibt den Namen der Ressourcengruppe an, die das Batchkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="4df94-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="4df94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df94-129">CommonParameters</span></span>
<span data-ttu-id="4df94-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df94-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4df94-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df94-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4df94-132">INPUTS</span></span>

### <span data-ttu-id="4df94-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4df94-133">System.String</span></span>

### <span data-ttu-id="4df94-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4df94-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4df94-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4df94-135">OUTPUTS</span></span>

### <span data-ttu-id="4df94-136">Microsoft.Azure.Commands.Batch. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4df94-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="4df94-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4df94-137">NOTES</span></span>

## <span data-ttu-id="4df94-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4df94-138">RELATED LINKS</span></span>

[<span data-ttu-id="4df94-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4df94-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="4df94-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4df94-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="4df94-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4df94-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="4df94-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4df94-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="4df94-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="4df94-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="4df94-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="4df94-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


