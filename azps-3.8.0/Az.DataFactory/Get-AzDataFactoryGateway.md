---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004760"
---
# <span data-ttu-id="f4294-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f4294-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="f4294-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4294-102">SYNOPSIS</span></span>
<span data-ttu-id="f4294-103">Ruft Informationen zu logischen Gateways in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="f4294-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="f4294-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4294-104">SYNTAX</span></span>

### <span data-ttu-id="f4294-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4294-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4294-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f4294-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4294-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4294-107">DESCRIPTION</span></span>
<span data-ttu-id="f4294-108">Das Cmdlet " **Get-AzDataFactoryGateway** " Ruft Informationen zu logischen Gateways in Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="f4294-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="f4294-109">Wenn Sie den Namen eines Gateways angeben, ruft dieses Cmdlet Informationen zu diesem Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="f4294-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="f4294-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Gateways für eine Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="f4294-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="f4294-111">Wenn Sie eine lokale Microsoft SQL Server-Datei als verknüpfter Dienst zu einer Data Factory hinzufügen möchten, müssen Sie ein Gateway auf dem lokalen Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="f4294-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="f4294-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4294-112">EXAMPLES</span></span>

### <span data-ttu-id="f4294-113">Beispiel 1: Abrufen aller logischen Gateways in einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="f4294-113">Example 1: Get all logical gateways in a data factory</span></span>
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

<span data-ttu-id="f4294-114">Dieser Befehl ruft Informationen zu allen logischen Gateways für die Data Factory mit dem Namen WikiADF in der Ressourcengruppe ADF ab.</span><span class="sxs-lookup"><span data-stu-id="f4294-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="f4294-115">Beispiel 2: Abrufen eines bestimmten logischen Gateways in einer Data Factory</span><span class="sxs-lookup"><span data-stu-id="f4294-115">Example 2: Get a specific logical gateway in a data factory</span></span>
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

<span data-ttu-id="f4294-116">Dieser Befehl ruft Informationen über das logische Gateway mit dem Namen Gateway01 in der Data Factory mit dem Namen WikiADF in der Ressourcengruppe "ADF" ab.</span><span class="sxs-lookup"><span data-stu-id="f4294-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="f4294-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4294-117">PARAMETERS</span></span>

### <span data-ttu-id="f4294-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4294-118">-DataFactory</span></span>
<span data-ttu-id="f4294-119">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f4294-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f4294-120">Dieses Cmdlet ruft Informationen zu logischen Gateways in der Data Factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f4294-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4294-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f4294-121">-DataFactoryName</span></span>
<span data-ttu-id="f4294-122">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="f4294-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f4294-123">Dieses Cmdlet ruft Informationen zu logischen Gateways in der Data Factory ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f4294-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4294-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4294-124">-DefaultProfile</span></span>
<span data-ttu-id="f4294-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f4294-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4294-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f4294-126">-Name</span></span>
<span data-ttu-id="f4294-127">Gibt den Namen des logischen Gateways an, für das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f4294-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="f4294-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4294-128">-ResourceGroupName</span></span>
<span data-ttu-id="f4294-129">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f4294-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f4294-130">Dieses Cmdlet ruft Informationen zu logischen Gateways ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f4294-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4294-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4294-131">CommonParameters</span></span>
<span data-ttu-id="f4294-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4294-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4294-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4294-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4294-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4294-134">INPUTS</span></span>

### <span data-ttu-id="f4294-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f4294-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f4294-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f4294-136">System.String</span></span>

## <span data-ttu-id="f4294-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4294-137">OUTPUTS</span></span>

### <span data-ttu-id="f4294-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f4294-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="f4294-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4294-139">NOTES</span></span>
* <span data-ttu-id="f4294-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="f4294-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f4294-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4294-141">RELATED LINKS</span></span>

[<span data-ttu-id="f4294-142">Neu – AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f4294-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="f4294-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f4294-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="f4294-144">Satz-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f4294-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


