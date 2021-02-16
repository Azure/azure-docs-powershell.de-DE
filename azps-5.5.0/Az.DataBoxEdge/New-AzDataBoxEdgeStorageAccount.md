---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 2a5a1314f422a7b91a5cc8885abe0af98fa395a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163852"
---
# <span data-ttu-id="a32b8-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a32b8-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="a32b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a32b8-102">SYNOPSIS</span></span>
<span data-ttu-id="a32b8-103">Erstellt ein neues Edgespeicherkonto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="a32b8-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="a32b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a32b8-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a32b8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a32b8-105">DESCRIPTION</span></span>
<span data-ttu-id="a32b8-106">Das **Cmdlet "New-AzDataBoxEdgeStorageAccount"** erstellt ein neues Edgespeicherkonto auf einem Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="a32b8-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="a32b8-107">Bei einem Gerät kann mindestens ein Edgespeicherkonto nur einem Cloudspeicherkonto zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a32b8-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="a32b8-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a32b8-108">EXAMPLES</span></span>

### <span data-ttu-id="a32b8-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a32b8-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="a32b8-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a32b8-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="a32b8-111">2 EdgeStorageAccounts auf dem Gerät können nur ein Cloudspeicherkonto gemeinsam nutzen</span><span class="sxs-lookup"><span data-stu-id="a32b8-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="a32b8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a32b8-112">PARAMETERS</span></span>

### <span data-ttu-id="a32b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a32b8-113">-AsJob</span></span>
<span data-ttu-id="a32b8-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a32b8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a32b8-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="a32b8-115">-Cloud</span></span>
<span data-ttu-id="a32b8-116">Verwendet ein CloudStorageAccount für die Tiering-</span><span class="sxs-lookup"><span data-stu-id="a32b8-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="a32b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32b8-117">-DefaultProfile</span></span>
<span data-ttu-id="a32b8-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a32b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a32b8-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a32b8-119">-DeviceName</span></span>
<span data-ttu-id="a32b8-120">Gerätename</span><span class="sxs-lookup"><span data-stu-id="a32b8-120">Device Name</span></span>

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

### <span data-ttu-id="a32b8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a32b8-121">-Name</span></span>
<span data-ttu-id="a32b8-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="a32b8-122">Resource Name</span></span>

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

### <span data-ttu-id="a32b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="a32b8-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a32b8-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a32b8-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="a32b8-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="a32b8-126">Bereitstellen des Ressourcennamens von StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a32b8-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="a32b8-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a32b8-127">-Confirm</span></span>
<span data-ttu-id="a32b8-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a32b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a32b8-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a32b8-129">-WhatIf</span></span>
<span data-ttu-id="a32b8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a32b8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a32b8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a32b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a32b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32b8-132">CommonParameters</span></span>
<span data-ttu-id="a32b8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a32b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32b8-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a32b8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32b8-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a32b8-135">INPUTS</span></span>

### <span data-ttu-id="a32b8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a32b8-136">System.String</span></span>

### <span data-ttu-id="a32b8-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a32b8-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a32b8-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a32b8-138">OUTPUTS</span></span>

### <span data-ttu-id="a32b8-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a32b8-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="a32b8-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a32b8-140">NOTES</span></span>

## <span data-ttu-id="a32b8-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a32b8-141">RELATED LINKS</span></span>
