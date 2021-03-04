---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 24c9f9631f1a37e218ff8ddf27ad0de54f2d9dbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930328"
---
# <span data-ttu-id="c58a5-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c58a5-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="c58a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c58a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c58a5-103">Ruft Informationen zu Hubs in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="c58a5-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="c58a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c58a5-104">SYNTAX</span></span>

### <span data-ttu-id="c58a5-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c58a5-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c58a5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c58a5-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c58a5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c58a5-107">DESCRIPTION</span></span>
<span data-ttu-id="c58a5-108">Das **Get-AzDataFactoryHub-Cmdlet** ruft Informationen zu Hubs in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="c58a5-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="c58a5-109">Wenn Sie den Namen eines Hubs angeben, ruft dieses Cmdlet Informationen zu diesem Hub ab.</span><span class="sxs-lookup"><span data-stu-id="c58a5-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="c58a5-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Hubs in einer Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="c58a5-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="c58a5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c58a5-111">EXAMPLES</span></span>

### <span data-ttu-id="c58a5-112">Beispiel 1: Alle Datenhubs erhalten</span><span class="sxs-lookup"><span data-stu-id="c58a5-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="c58a5-113">Dieser Befehl ruft alle Datenhubs in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Datenfactory mit dem Namen ADFDataFactory ab.</span><span class="sxs-lookup"><span data-stu-id="c58a5-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="c58a5-114">Beispiel 2: Erhalten eines bestimmten Datenhubs</span><span class="sxs-lookup"><span data-stu-id="c58a5-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="c58a5-115">Dieser Befehl ruft Informationen zum Hub mit dem Namen MyDataHub in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Datenfactory mit dem Namen ADFDataFactory ab.</span><span class="sxs-lookup"><span data-stu-id="c58a5-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="c58a5-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c58a5-116">PARAMETERS</span></span>

### <span data-ttu-id="c58a5-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c58a5-117">-DataFactory</span></span>
<span data-ttu-id="c58a5-118">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="c58a5-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c58a5-119">Dieses Cmdlet ruft Informationen zu Hubs in der Daten factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c58a5-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c58a5-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c58a5-120">-DataFactoryName</span></span>
<span data-ttu-id="c58a5-121">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="c58a5-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c58a5-122">Dieses Cmdlet ruft Informationen zu Hubs in der Daten factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c58a5-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c58a5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c58a5-123">-DefaultProfile</span></span>
<span data-ttu-id="c58a5-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c58a5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c58a5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c58a5-125">-Name</span></span>
<span data-ttu-id="c58a5-126">Gibt den Namen des Hubs an, über den Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="c58a5-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c58a5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c58a5-127">-ResourceGroupName</span></span>
<span data-ttu-id="c58a5-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c58a5-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c58a5-129">Dieses Cmdlet ruft Informationen zu Hubs ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c58a5-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c58a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c58a5-130">CommonParameters</span></span>
<span data-ttu-id="c58a5-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c58a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c58a5-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c58a5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c58a5-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c58a5-133">INPUTS</span></span>

### <span data-ttu-id="c58a5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c58a5-134">System.String</span></span>

### <span data-ttu-id="c58a5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c58a5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="c58a5-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c58a5-136">OUTPUTS</span></span>

### <span data-ttu-id="c58a5-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="c58a5-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="c58a5-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c58a5-138">NOTES</span></span>
* <span data-ttu-id="c58a5-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="c58a5-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c58a5-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c58a5-140">RELATED LINKS</span></span>

[<span data-ttu-id="c58a5-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c58a5-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="c58a5-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c58a5-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


