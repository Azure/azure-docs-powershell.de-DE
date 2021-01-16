---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307499"
---
# <span data-ttu-id="1ace0-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="1ace0-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="1ace0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ace0-102">SYNOPSIS</span></span>
<span data-ttu-id="1ace0-103">Ruft Informationen zu Hubs in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="1ace0-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="1ace0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ace0-104">SYNTAX</span></span>

### <span data-ttu-id="1ace0-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ace0-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ace0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1ace0-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ace0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ace0-107">DESCRIPTION</span></span>
<span data-ttu-id="1ace0-108">Das **Get-AzDataFactoryHub-Cmdlet** ruft Informationen zu Hubs in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="1ace0-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="1ace0-109">Wenn Sie den Namen eines Hubs angeben, ruft dieses Cmdlet Informationen zu diesem Hub ab.</span><span class="sxs-lookup"><span data-stu-id="1ace0-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="1ace0-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Hubs in einer Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="1ace0-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="1ace0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ace0-111">EXAMPLES</span></span>

### <span data-ttu-id="1ace0-112">Beispiel 1: Alle Datenhubs erhalten</span><span class="sxs-lookup"><span data-stu-id="1ace0-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="1ace0-113">Dieser Befehl ruft alle Datenhubs in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Datenfactory mit dem Namen ADFDataFactory ab.</span><span class="sxs-lookup"><span data-stu-id="1ace0-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="1ace0-114">Beispiel 2: Erhalten eines bestimmten Datenhubs</span><span class="sxs-lookup"><span data-stu-id="1ace0-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="1ace0-115">Dieser Befehl ruft Informationen über den Hub mit dem Namen "MyDataHub" in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Datenfactory mit dem Namen ADFDataFactory ab.</span><span class="sxs-lookup"><span data-stu-id="1ace0-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="1ace0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ace0-116">PARAMETERS</span></span>

### <span data-ttu-id="1ace0-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ace0-117">-DataFactory</span></span>
<span data-ttu-id="1ace0-118">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="1ace0-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1ace0-119">Dieses Cmdlet ruft Informationen zu Hubs in der Daten factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1ace0-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ace0-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1ace0-120">-DataFactoryName</span></span>
<span data-ttu-id="1ace0-121">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="1ace0-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1ace0-122">Dieses Cmdlet ruft Informationen zu Hubs in der Daten factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1ace0-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ace0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ace0-123">-DefaultProfile</span></span>
<span data-ttu-id="1ace0-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1ace0-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ace0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1ace0-125">-Name</span></span>
<span data-ttu-id="1ace0-126">Gibt den Namen des Hubs an, über den Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1ace0-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="1ace0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ace0-127">-ResourceGroupName</span></span>
<span data-ttu-id="1ace0-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1ace0-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1ace0-129">Dieses Cmdlet ruft Informationen zu Hubs ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1ace0-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ace0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ace0-130">CommonParameters</span></span>
<span data-ttu-id="1ace0-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ace0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ace0-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ace0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ace0-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ace0-133">INPUTS</span></span>

### <span data-ttu-id="1ace0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1ace0-134">System.String</span></span>

### <span data-ttu-id="1ace0-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1ace0-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1ace0-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ace0-136">OUTPUTS</span></span>

### <span data-ttu-id="1ace0-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="1ace0-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="1ace0-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1ace0-138">NOTES</span></span>
* <span data-ttu-id="1ace0-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="1ace0-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1ace0-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1ace0-140">RELATED LINKS</span></span>

[<span data-ttu-id="1ace0-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="1ace0-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="1ace0-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="1ace0-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


