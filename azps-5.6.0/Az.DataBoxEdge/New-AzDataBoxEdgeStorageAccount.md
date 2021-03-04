---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: c0cea590ced7abdaad1021453304ea1508790b55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931915"
---
# <span data-ttu-id="17427-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17427-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="17427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17427-102">SYNOPSIS</span></span>
<span data-ttu-id="17427-103">Erstellt ein neues Edgespeicherkonto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="17427-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="17427-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17427-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17427-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17427-105">DESCRIPTION</span></span>
<span data-ttu-id="17427-106">Das **Cmdlet New-AzDataBoxEdgeStorageAccount** erstellt ein neues Edgespeicherkonto auf einem Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="17427-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="17427-107">Bei einem Gerät kann ein Edgespeicherkonto bestens nur einem Cloudspeicherkonto zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="17427-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="17427-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17427-108">EXAMPLES</span></span>

### <span data-ttu-id="17427-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17427-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="17427-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="17427-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="17427-111">2 EdgeStorageAccounts auf dem Gerät dürfen nicht mehr als 1 Cloudspeicherkonto freigeben</span><span class="sxs-lookup"><span data-stu-id="17427-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="17427-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="17427-112">PARAMETERS</span></span>

### <span data-ttu-id="17427-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17427-113">-AsJob</span></span>
<span data-ttu-id="17427-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="17427-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17427-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="17427-115">-Cloud</span></span>
<span data-ttu-id="17427-116">Verwendet ein CloudStorageAccount für die Tiering</span><span class="sxs-lookup"><span data-stu-id="17427-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="17427-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17427-117">-DefaultProfile</span></span>
<span data-ttu-id="17427-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17427-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17427-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="17427-119">-DeviceName</span></span>
<span data-ttu-id="17427-120">Gerätename</span><span class="sxs-lookup"><span data-stu-id="17427-120">Device Name</span></span>

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

### <span data-ttu-id="17427-121">-Name</span><span class="sxs-lookup"><span data-stu-id="17427-121">-Name</span></span>
<span data-ttu-id="17427-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="17427-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17427-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17427-123">-ResourceGroupName</span></span>
<span data-ttu-id="17427-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="17427-124">Resource Group Name</span></span>

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

### <span data-ttu-id="17427-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="17427-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="17427-126">Bereitstellen des Ressourcennamens von StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="17427-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17427-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17427-127">-Confirm</span></span>
<span data-ttu-id="17427-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17427-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17427-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17427-129">-WhatIf</span></span>
<span data-ttu-id="17427-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17427-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17427-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17427-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17427-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17427-132">CommonParameters</span></span>
<span data-ttu-id="17427-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17427-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17427-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17427-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17427-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17427-135">INPUTS</span></span>

### <span data-ttu-id="17427-136">System.String</span><span class="sxs-lookup"><span data-stu-id="17427-136">System.String</span></span>

### <span data-ttu-id="17427-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="17427-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="17427-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17427-138">OUTPUTS</span></span>

### <span data-ttu-id="17427-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17427-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="17427-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="17427-140">NOTES</span></span>

## <span data-ttu-id="17427-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="17427-141">RELATED LINKS</span></span>
