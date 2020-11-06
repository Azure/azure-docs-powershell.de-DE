---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: d1015a5f401b0cb91731bafe93ead02e2bf3068f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504446"
---
# <span data-ttu-id="b5578-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="b5578-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="b5578-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5578-102">SYNOPSIS</span></span>
<span data-ttu-id="b5578-103">Ruft Informationen zu Hubs in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b5578-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5578-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5578-104">SYNTAX</span></span>

### <span data-ttu-id="b5578-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5578-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5578-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b5578-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5578-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5578-107">DESCRIPTION</span></span>
<span data-ttu-id="b5578-108">Das Cmdlet " **Get-AzureRmDataFactoryHub** " Ruft Informationen zu Hubs in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b5578-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="b5578-109">Wenn Sie den Namen eines Hubs angeben, ruft dieses Cmdlet Informationen zu diesem Hub ab.</span><span class="sxs-lookup"><span data-stu-id="b5578-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="b5578-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Hubs in einer Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="b5578-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="b5578-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5578-111">EXAMPLES</span></span>

### <span data-ttu-id="b5578-112">Beispiel 1: Abrufen aller Daten Hubs</span><span class="sxs-lookup"><span data-stu-id="b5578-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="b5578-113">Dieser Befehl ruft alle Daten Hubs in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Data Factory mit dem Namen ADFDataFactory ab.</span><span class="sxs-lookup"><span data-stu-id="b5578-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="b5578-114">Beispiel 2: Abrufen eines bestimmten Daten Hubs</span><span class="sxs-lookup"><span data-stu-id="b5578-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="b5578-115">Dieser Befehl ruft Informationen zu dem Hub mit dem Namen MyDataHub in der Azure-Ressourcengruppe mit dem Namen ADFResourceGroup und der Data Factory mit dem Namen ADFDataFactory ab.</span><span class="sxs-lookup"><span data-stu-id="b5578-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="b5578-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5578-116">PARAMETERS</span></span>

### <span data-ttu-id="b5578-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b5578-117">-DataFactory</span></span>
<span data-ttu-id="b5578-118">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b5578-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b5578-119">Dieses Cmdlet ruft Informationen zu Hubs in der Data Factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b5578-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b5578-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b5578-120">-DataFactoryName</span></span>
<span data-ttu-id="b5578-121">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="b5578-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b5578-122">Dieses Cmdlet ruft Informationen zu Hubs in der Data Factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b5578-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b5578-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5578-123">-DefaultProfile</span></span>
<span data-ttu-id="b5578-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b5578-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5578-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b5578-125">-Name</span></span>
<span data-ttu-id="b5578-126">Gibt den Namen des Hubs an, über den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b5578-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="b5578-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5578-127">-ResourceGroupName</span></span>
<span data-ttu-id="b5578-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b5578-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b5578-129">Dieses Cmdlet ruft Informationen zu Hubs ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b5578-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b5578-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5578-130">CommonParameters</span></span>
<span data-ttu-id="b5578-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5578-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5578-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5578-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5578-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5578-133">INPUTS</span></span>

### <span data-ttu-id="b5578-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b5578-134">System.String</span></span>

### <span data-ttu-id="b5578-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b5578-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="b5578-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5578-136">OUTPUTS</span></span>

### <span data-ttu-id="b5578-137">Microsoft. Azure. Commands. datafactoring. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="b5578-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="b5578-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5578-138">NOTES</span></span>
* <span data-ttu-id="b5578-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="b5578-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b5578-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5578-140">RELATED LINKS</span></span>

[<span data-ttu-id="b5578-141">Neu – AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="b5578-141">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="b5578-142">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="b5578-142">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


