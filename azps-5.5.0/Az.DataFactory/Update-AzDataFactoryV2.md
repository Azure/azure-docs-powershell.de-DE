---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 57c0a05c5b0f279fa7c9f06cd561385de87698bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153457"
---
# <span data-ttu-id="92f92-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="92f92-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="92f92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92f92-102">SYNOPSIS</span></span>
<span data-ttu-id="92f92-103">Aktualisiert die Eigenschaften einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="92f92-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="92f92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92f92-104">SYNTAX</span></span>

### <span data-ttu-id="92f92-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="92f92-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92f92-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="92f92-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92f92-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="92f92-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92f92-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92f92-108">DESCRIPTION</span></span>
<span data-ttu-id="92f92-109">Das **Cmdlet "Update-AzDataFactoryV2"** aktualisiert Tags oder Identitätseigenschaften einer Datenfactory.</span><span class="sxs-lookup"><span data-stu-id="92f92-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="92f92-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92f92-110">EXAMPLES</span></span>

### <span data-ttu-id="92f92-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92f92-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="92f92-112">Mit diesem Befehl werden die Tags für das #A0 in ein Wörterbuch aktualisiert, das ein Tag namens "myNewTagName" mit dem Wert "myTagValue" enthält.</span><span class="sxs-lookup"><span data-stu-id="92f92-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="92f92-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92f92-113">PARAMETERS</span></span>

### <span data-ttu-id="92f92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f92-114">-DefaultProfile</span></span>
<span data-ttu-id="92f92-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92f92-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92f92-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92f92-116">-InputObject</span></span>
<span data-ttu-id="92f92-117">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="92f92-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92f92-118">-Name</span><span class="sxs-lookup"><span data-stu-id="92f92-118">-Name</span></span>
<span data-ttu-id="92f92-119">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="92f92-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f92-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f92-120">-ResourceGroupName</span></span>
<span data-ttu-id="92f92-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="92f92-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f92-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92f92-122">-ResourceId</span></span>
<span data-ttu-id="92f92-123">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="92f92-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f92-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="92f92-124">-Tag</span></span>
<span data-ttu-id="92f92-125">Die Tags der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="92f92-125">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f92-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92f92-126">-Confirm</span></span>
<span data-ttu-id="92f92-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92f92-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92f92-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="92f92-128">-WhatIf</span></span>
<span data-ttu-id="92f92-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92f92-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92f92-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92f92-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92f92-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f92-131">CommonParameters</span></span>
<span data-ttu-id="92f92-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f92-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f92-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f92-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f92-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92f92-134">INPUTS</span></span>

### <span data-ttu-id="92f92-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="92f92-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="92f92-136">System.String</span><span class="sxs-lookup"><span data-stu-id="92f92-136">System.String</span></span>

## <span data-ttu-id="92f92-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92f92-137">OUTPUTS</span></span>

### <span data-ttu-id="92f92-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="92f92-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="92f92-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="92f92-139">NOTES</span></span>

## <span data-ttu-id="92f92-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="92f92-140">RELATED LINKS</span></span>
