---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144380"
---
# <span data-ttu-id="fbb9b-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fbb9b-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="fbb9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb9b-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb9b-103">Legt die Beschreibung für ein Gateway in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="fbb9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbb9b-104">SYNTAX</span></span>

### <span data-ttu-id="fbb9b-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbb9b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbb9b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fbb9b-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbb9b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbb9b-107">DESCRIPTION</span></span>
<span data-ttu-id="fbb9b-108">Das **Cmdlet Set-AzDataFactoryGateway** legt die Beschreibung für das angegebene Gateway in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="fbb9b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbb9b-109">EXAMPLES</span></span>

### <span data-ttu-id="fbb9b-110">Beispiel 1: Festlegen der Beschreibung für ein Gateway</span><span class="sxs-lookup"><span data-stu-id="fbb9b-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="fbb9b-111">Mit diesem Befehl wird die Beschreibung für das Gateway mit dem Namen "ContosoGateway" in der Daten factory namens WikiADF bestimmt.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="fbb9b-112">Der Parameter "Description" gibt die neue Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="fbb9b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbb9b-113">PARAMETERS</span></span>

### <span data-ttu-id="fbb9b-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fbb9b-114">-DataFactory</span></span>
<span data-ttu-id="fbb9b-115">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fbb9b-116">Dieses Cmdlet legt die Beschreibung für das Gateway in der Daten factory fest, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbb9b-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fbb9b-117">-DataFactoryName</span></span>
<span data-ttu-id="fbb9b-118">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fbb9b-119">Dieses Cmdlet legt die Beschreibung für das Gateway in der Daten factory fest, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbb9b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb9b-120">-DefaultProfile</span></span>
<span data-ttu-id="fbb9b-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fbb9b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbb9b-122">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb9b-122">-Description</span></span>
<span data-ttu-id="fbb9b-123">Gibt eine Beschreibung für das Gateway an.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb9b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fbb9b-124">-Name</span></span>
<span data-ttu-id="fbb9b-125">Gibt den Namen des Gateways an, für das eine Beschreibung festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-125">Specifies the name of the gateway for which to set a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb9b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb9b-126">-ResourceGroupName</span></span>
<span data-ttu-id="fbb9b-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fbb9b-128">Dieses Cmdlet legt die Beschreibung für ein Gateway fest, das zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbb9b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb9b-129">CommonParameters</span></span>
<span data-ttu-id="fbb9b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb9b-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb9b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb9b-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbb9b-132">INPUTS</span></span>

### <span data-ttu-id="fbb9b-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fbb9b-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="fbb9b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fbb9b-134">System.String</span></span>

## <span data-ttu-id="fbb9b-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbb9b-135">OUTPUTS</span></span>

### <span data-ttu-id="fbb9b-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fbb9b-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="fbb9b-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbb9b-137">NOTES</span></span>
* <span data-ttu-id="fbb9b-138">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="fbb9b-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fbb9b-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbb9b-139">RELATED LINKS</span></span>

[<span data-ttu-id="fbb9b-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fbb9b-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="fbb9b-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fbb9b-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="fbb9b-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fbb9b-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


