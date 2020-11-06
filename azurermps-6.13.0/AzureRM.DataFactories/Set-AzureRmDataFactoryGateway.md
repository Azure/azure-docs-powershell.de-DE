---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: c40999dfa9f1300502e8909a32eaf13a34d0bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499634"
---
# <span data-ttu-id="98c07-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="98c07-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="98c07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98c07-102">SYNOPSIS</span></span>
<span data-ttu-id="98c07-103">Legt die Beschreibung für ein Gateway in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="98c07-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98c07-104">SYNTAX</span></span>

### <span data-ttu-id="98c07-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="98c07-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98c07-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="98c07-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c07-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98c07-107">DESCRIPTION</span></span>
<span data-ttu-id="98c07-108">Das Cmdlet " **Set-AzureRmDataFactoryGateway** " legt die Beschreibung für das angegebene Gateway in Azure Data Factory fest.</span><span class="sxs-lookup"><span data-stu-id="98c07-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="98c07-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98c07-109">EXAMPLES</span></span>

### <span data-ttu-id="98c07-110">Beispiel 1: Einrichten der Beschreibung für ein Gateway</span><span class="sxs-lookup"><span data-stu-id="98c07-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="98c07-111">Mit diesem Befehl wird die Beschreibung für das Gateway mit dem Namen ContosoGateway in der Data Factory mit dem Namen WikiADF festgelegt.</span><span class="sxs-lookup"><span data-stu-id="98c07-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="98c07-112">Der Parameter Description gibt die neue Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="98c07-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="98c07-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="98c07-113">PARAMETERS</span></span>

### <span data-ttu-id="98c07-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="98c07-114">-DataFactory</span></span>
<span data-ttu-id="98c07-115">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="98c07-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="98c07-116">Mit diesem Cmdlet wird die Beschreibung für das Gateway in der Data Factory festgelegt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="98c07-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98c07-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="98c07-117">-DataFactoryName</span></span>
<span data-ttu-id="98c07-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="98c07-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="98c07-119">Mit diesem Cmdlet wird die Beschreibung für das Gateway in der Data Factory festgelegt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="98c07-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98c07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c07-120">-DefaultProfile</span></span>
<span data-ttu-id="98c07-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="98c07-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98c07-122">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98c07-122">-Description</span></span>
<span data-ttu-id="98c07-123">Gibt eine Beschreibung für das Gateway an.</span><span class="sxs-lookup"><span data-stu-id="98c07-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="98c07-124">-Name</span><span class="sxs-lookup"><span data-stu-id="98c07-124">-Name</span></span>
<span data-ttu-id="98c07-125">Gibt den Namen des Gateways an, für das eine Beschreibung festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="98c07-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="98c07-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c07-126">-ResourceGroupName</span></span>
<span data-ttu-id="98c07-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="98c07-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="98c07-128">Mit diesem Cmdlet wird die Beschreibung für ein Gateway festgelegt, das zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="98c07-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="98c07-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c07-129">CommonParameters</span></span>
<span data-ttu-id="98c07-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c07-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c07-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c07-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c07-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98c07-132">INPUTS</span></span>

### <span data-ttu-id="98c07-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="98c07-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="98c07-134">System. String</span><span class="sxs-lookup"><span data-stu-id="98c07-134">System.String</span></span>

## <span data-ttu-id="98c07-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98c07-135">OUTPUTS</span></span>

### <span data-ttu-id="98c07-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="98c07-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="98c07-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="98c07-137">NOTES</span></span>
* <span data-ttu-id="98c07-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="98c07-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="98c07-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98c07-139">RELATED LINKS</span></span>

[<span data-ttu-id="98c07-140">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="98c07-140">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="98c07-141">Neu – AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="98c07-141">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="98c07-142">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="98c07-142">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


