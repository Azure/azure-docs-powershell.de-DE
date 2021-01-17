---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472692"
---
# <span data-ttu-id="8f9c7-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="8f9c7-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="8f9c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8f9c7-103">Ruft den Gatewayauthentifizierungsschlüssel für eine Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="8f9c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f9c7-104">SYNTAX</span></span>

### <span data-ttu-id="8f9c7-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f9c7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f9c7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8f9c7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f9c7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f9c7-107">DESCRIPTION</span></span>
<span data-ttu-id="8f9c7-108">Das **Cmdlet "Get-AzDataFactoryGatewayAuthKey"** ruft den Gatewayauthentifizierungsschlüssel für ein angegebenes Azure Data Factory-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="8f9c7-109">Sie registrieren das Gateway bei einem Clouddienst, indem Sie diesen Schlüssel1 oder Schlüssel2 dieses Authentifizierungsschlüssels verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="8f9c7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f9c7-110">EXAMPLES</span></span>

### <span data-ttu-id="8f9c7-111">Beispiel 1: Ruft den Authentifizierungsschlüssel eines Gateways ab</span><span class="sxs-lookup"><span data-stu-id="8f9c7-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="8f9c7-112">Dieser Befehl ruft den Gatewayauthentifizierungsschlüssel für das Daten factorygateway namens "MyGateway" ab.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="8f9c7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f9c7-113">PARAMETERS</span></span>

### <span data-ttu-id="8f9c7-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8f9c7-114">-DataFactoryName</span></span>
<span data-ttu-id="8f9c7-115">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-115">The data factory name.</span></span>

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

### <span data-ttu-id="8f9c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f9c7-116">-DefaultProfile</span></span>
<span data-ttu-id="8f9c7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8f9c7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f9c7-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="8f9c7-118">-GatewayName</span></span>
<span data-ttu-id="8f9c7-119">Der Name des Daten factorygateways.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="8f9c7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f9c7-120">-InputObject</span></span>
<span data-ttu-id="8f9c7-121">Das Data Factory-Objekt</span><span class="sxs-lookup"><span data-stu-id="8f9c7-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f9c7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f9c7-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f9c7-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-123">The resource group name.</span></span>

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

### <span data-ttu-id="8f9c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f9c7-124">CommonParameters</span></span>
<span data-ttu-id="8f9c7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f9c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f9c7-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f9c7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f9c7-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f9c7-127">INPUTS</span></span>

### <span data-ttu-id="8f9c7-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8f9c7-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="8f9c7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8f9c7-129">System.String</span></span>

## <span data-ttu-id="8f9c7-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f9c7-130">OUTPUTS</span></span>

### <span data-ttu-id="8f9c7-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="8f9c7-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="8f9c7-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f9c7-132">NOTES</span></span>
* <span data-ttu-id="8f9c7-133">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="8f9c7-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8f9c7-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f9c7-134">RELATED LINKS</span></span>

<span data-ttu-id="8f9c7-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="8f9c7-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

