---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: d360a468d69306b5f203cbd28d17e9bfcc00bdcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478546"
---
# <span data-ttu-id="d7642-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d7642-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="d7642-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7642-102">SYNOPSIS</span></span>
<span data-ttu-id="d7642-103">Erstellt einen gatewayschlüssel für eine Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7642-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="d7642-104">Dieses Cmdlet ist veraltet, und stattdessen sollten Sie **New-AzureRmDataFactoryGatewayAuthKey** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7642-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7642-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7642-105">SYNTAX</span></span>

### <span data-ttu-id="d7642-106">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7642-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7642-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d7642-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7642-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7642-108">DESCRIPTION</span></span>
<span data-ttu-id="d7642-109">Das Cmdlet **New-AzureRmDataFactoryGatewayKey** erstellt einen gatewayschlüssel für ein angegebenes Azure Data Factory-Gateway.</span><span class="sxs-lookup"><span data-stu-id="d7642-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="d7642-110">Mit diesem Schlüssel registrieren Sie das Gateway bei einem clouddienst.</span><span class="sxs-lookup"><span data-stu-id="d7642-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="d7642-111">Dieses Cmdlet ist veraltet, und stattdessen sollten Sie **New-AzureRmDataFactoryGatewayAuthKey** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7642-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="d7642-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7642-112">EXAMPLES</span></span>

### <span data-ttu-id="d7642-113">Beispiel 1: Erstellen eines Gateway-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d7642-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="d7642-114">Dieser Befehl erstellt einen gatewayschlüssel für das Data Factory-Gateway mit dem Namen ContosoGateway und übergibt dann den gatewayschlüssel mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7642-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7642-115">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="d7642-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="d7642-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7642-116">PARAMETERS</span></span>

### <span data-ttu-id="d7642-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d7642-117">-DataFactory</span></span>
<span data-ttu-id="d7642-118">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d7642-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d7642-119">Dieses Cmdlet erstellt einen Gateway-Schlüssel für die Data Factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7642-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7642-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d7642-120">-DataFactoryName</span></span>
<span data-ttu-id="d7642-121">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="d7642-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d7642-122">Dieses Cmdlet erstellt einen Gateway-Schlüssel für die Data Factory, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7642-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7642-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7642-123">-DefaultProfile</span></span>
<span data-ttu-id="d7642-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7642-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7642-125">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="d7642-125">-GatewayName</span></span>
<span data-ttu-id="d7642-126">Gibt den Namen des Gateways an.</span><span class="sxs-lookup"><span data-stu-id="d7642-126">Specifies the name of the gateway.</span></span>
<span data-ttu-id="d7642-127">Dieses Cmdlet erstellt einen Schlüssel für das Gateway, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7642-127">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7642-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7642-128">-ResourceGroupName</span></span>
<span data-ttu-id="d7642-129">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d7642-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d7642-130">Dieses Cmdlet erstellt einen Schlüssel für ein Gateway, das zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7642-130">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7642-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7642-131">CommonParameters</span></span>
<span data-ttu-id="d7642-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7642-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7642-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7642-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7642-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7642-134">INPUTS</span></span>

### <span data-ttu-id="d7642-135">Keine</span><span class="sxs-lookup"><span data-stu-id="d7642-135">None</span></span>
<span data-ttu-id="d7642-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d7642-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7642-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7642-137">OUTPUTS</span></span>

### <span data-ttu-id="d7642-138">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="d7642-138">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="d7642-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7642-139">NOTES</span></span>
* <span data-ttu-id="d7642-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="d7642-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d7642-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7642-141">RELATED LINKS</span></span>

<span data-ttu-id="d7642-142">[Neu – AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [Neu – AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="d7642-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>


