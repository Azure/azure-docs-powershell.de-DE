---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 80ff3a13014bcdc05191bcf5555abf2e029a831d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930336"
---
# <span data-ttu-id="e71dd-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e71dd-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="e71dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e71dd-102">SYNOPSIS</span></span>
<span data-ttu-id="e71dd-103">Ruft Informationen zu logischen Gateways in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="e71dd-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="e71dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e71dd-104">SYNTAX</span></span>

### <span data-ttu-id="e71dd-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e71dd-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e71dd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e71dd-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e71dd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e71dd-107">DESCRIPTION</span></span>
<span data-ttu-id="e71dd-108">Das **Get-AzDataFactoryGateway-Cmdlet** ruft Informationen zu logischen Gateways in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="e71dd-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="e71dd-109">Wenn Sie den Namen eines Gateways angeben, ruft dieses Cmdlet Informationen zu diesem Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="e71dd-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="e71dd-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Gateways für eine Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="e71dd-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="e71dd-111">Wenn Sie einer Daten factory eine lokale Microsoft SQL Server als verknüpften Dienst hinzufügen möchten, müssen Sie ein Gateway auf Ihrem lokalen Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="e71dd-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="e71dd-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e71dd-112">EXAMPLES</span></span>

### <span data-ttu-id="e71dd-113">Beispiel 1: Alle logischen Gateways in einer Daten factory</span><span class="sxs-lookup"><span data-stu-id="e71dd-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="e71dd-114">Dieser Befehl ruft Informationen zu allen logischen Gateways für die Daten factory namens WikiADF in der Ressourcengruppe mit dem Namen ADF ab.</span><span class="sxs-lookup"><span data-stu-id="e71dd-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="e71dd-115">Beispiel 2: Erhalten eines bestimmten logischen Gateways in einer Daten factory</span><span class="sxs-lookup"><span data-stu-id="e71dd-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="e71dd-116">Dieser Befehl ruft Informationen über das logische Gateway mit dem Namen Gateway01 in der Daten factory mit dem Namen WikiADF in der Ressourcengruppe mit dem Namen ADF ab.</span><span class="sxs-lookup"><span data-stu-id="e71dd-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="e71dd-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e71dd-117">PARAMETERS</span></span>

### <span data-ttu-id="e71dd-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e71dd-118">-DataFactory</span></span>
<span data-ttu-id="e71dd-119">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="e71dd-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e71dd-120">Dieses Cmdlet ruft Informationen zu logischen Gateways in der Daten factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e71dd-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e71dd-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e71dd-121">-DataFactoryName</span></span>
<span data-ttu-id="e71dd-122">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="e71dd-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e71dd-123">Dieses Cmdlet ruft Informationen zu logischen Gateways in der Daten factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e71dd-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e71dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71dd-124">-DefaultProfile</span></span>
<span data-ttu-id="e71dd-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e71dd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e71dd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e71dd-126">-Name</span></span>
<span data-ttu-id="e71dd-127">Gibt den Namen des logischen Gateways an, über das Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="e71dd-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="e71dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="e71dd-129">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e71dd-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e71dd-130">Dieses Cmdlet ruft Informationen zu logischen Gateways ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e71dd-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e71dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71dd-131">CommonParameters</span></span>
<span data-ttu-id="e71dd-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e71dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71dd-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e71dd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71dd-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e71dd-134">INPUTS</span></span>

### <span data-ttu-id="e71dd-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e71dd-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="e71dd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e71dd-136">System.String</span></span>

## <span data-ttu-id="e71dd-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e71dd-137">OUTPUTS</span></span>

### <span data-ttu-id="e71dd-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e71dd-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="e71dd-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e71dd-139">NOTES</span></span>
* <span data-ttu-id="e71dd-140">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="e71dd-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e71dd-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e71dd-141">RELATED LINKS</span></span>

[<span data-ttu-id="e71dd-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e71dd-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="e71dd-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e71dd-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="e71dd-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e71dd-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


