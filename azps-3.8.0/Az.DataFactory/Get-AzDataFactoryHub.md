---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004466"
---
# <span data-ttu-id="06314-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="06314-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="06314-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06314-102">SYNOPSIS</span></span>
<span data-ttu-id="06314-103">Ruft Informationen zu Hubs in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="06314-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="06314-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06314-104">SYNTAX</span></span>

### <span data-ttu-id="06314-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="06314-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06314-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="06314-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06314-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06314-107">DESCRIPTION</span></span>
<span data-ttu-id="06314-108">Das Cmdlet " **Get-AzDataFactoryHub** " Ruft Informationen zu Hubs in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="06314-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="06314-109">Wenn Sie den Namen eines Hubs angeben, ruft dieses Cmdlet Informationen zu diesem Hub ab.</span><span class="sxs-lookup"><span data-stu-id="06314-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="06314-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Hubs in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="06314-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="06314-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06314-111">EXAMPLES</span></span>

### <span data-ttu-id="06314-112">Beispiel 1: Abrufen aller Daten Hubs</span><span class="sxs-lookup"><span data-stu-id="06314-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="06314-113">Dieser Befehl ruft alle Daten Hubs in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Data Factory mit dem Namen ADFDataFactory ab.</span><span class="sxs-lookup"><span data-stu-id="06314-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="06314-114">Beispiel 2: Abrufen eines bestimmten Daten Hubs</span><span class="sxs-lookup"><span data-stu-id="06314-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="06314-115">Dieser Befehl ruft Informationen zu dem Hub mit dem Namen MyDataHub in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Data Factory mit dem Namen ADFDataFactory ab.</span><span class="sxs-lookup"><span data-stu-id="06314-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="06314-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="06314-116">PARAMETERS</span></span>

### <span data-ttu-id="06314-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="06314-117">-DataFactory</span></span>
<span data-ttu-id="06314-118">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="06314-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="06314-119">Dieses Cmdlet ruft Informationen zu Hubs in der Data Factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="06314-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="06314-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="06314-120">-DataFactoryName</span></span>
<span data-ttu-id="06314-121">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="06314-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="06314-122">Dieses Cmdlet ruft Informationen zu Hubs in der Data Factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="06314-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="06314-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06314-123">-DefaultProfile</span></span>
<span data-ttu-id="06314-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="06314-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06314-125">-Name</span><span class="sxs-lookup"><span data-stu-id="06314-125">-Name</span></span>
<span data-ttu-id="06314-126">Gibt den Namen des Hubs an, über den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="06314-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="06314-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06314-127">-ResourceGroupName</span></span>
<span data-ttu-id="06314-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="06314-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="06314-129">Dieses Cmdlet ruft Informationen zu Hubs ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="06314-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="06314-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06314-130">CommonParameters</span></span>
<span data-ttu-id="06314-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06314-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06314-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06314-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06314-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06314-133">INPUTS</span></span>

### <span data-ttu-id="06314-134">System. String</span><span class="sxs-lookup"><span data-stu-id="06314-134">System.String</span></span>

### <span data-ttu-id="06314-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="06314-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="06314-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06314-136">OUTPUTS</span></span>

### <span data-ttu-id="06314-137">Microsoft. Azure. Commands. datafactoring. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="06314-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="06314-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="06314-138">NOTES</span></span>
* <span data-ttu-id="06314-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="06314-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="06314-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06314-140">RELATED LINKS</span></span>

[<span data-ttu-id="06314-141">Neu – AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="06314-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="06314-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="06314-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


