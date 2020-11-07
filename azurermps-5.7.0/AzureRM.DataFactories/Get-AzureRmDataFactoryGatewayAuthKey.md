---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 9e677417ed1d592da04d8023a7cc58826662fada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662945"
---
# <span data-ttu-id="d8694-101">Get-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="d8694-101">Get-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="d8694-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8694-102">SYNOPSIS</span></span>
<span data-ttu-id="d8694-103">Ruft den Gateway-Authentifizierungsschlüssel für eine Azure Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="d8694-103">Gets gateway auth key for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8694-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8694-104">SYNTAX</span></span>

### <span data-ttu-id="d8694-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8694-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8694-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d8694-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8694-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8694-107">DESCRIPTION</span></span>
<span data-ttu-id="d8694-108">Das Cmdlet " **Get-AzureRmDataFactoryGatewayAuthKey** " Ruft den Gateway-Authentifizierungsschlüssel für ein angegebenes Azure Data Factory-Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="d8694-108">The **Get-AzureRmDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="d8694-109">Sie registrieren das Gateway mit einem clouddienst, indem Sie diesen key1 oder key2 dieses auth-Schlüssels verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8694-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="d8694-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8694-110">EXAMPLES</span></span>

### <span data-ttu-id="d8694-111">Beispiel 1: Ruft den auth-Schlüssel eines Gateways ab</span><span class="sxs-lookup"><span data-stu-id="d8694-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="d8694-112">Dieser Befehl ruft den Gateway-Authentifizierungsschlüssel für das Data Factory-Gateway mit dem Namen mygateway ab.</span><span class="sxs-lookup"><span data-stu-id="d8694-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="d8694-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8694-113">PARAMETERS</span></span>

### <span data-ttu-id="d8694-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d8694-114">-DataFactoryName</span></span>
<span data-ttu-id="d8694-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="d8694-115">The data factory name.</span></span>

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

### <span data-ttu-id="d8694-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8694-116">-DefaultProfile</span></span>
<span data-ttu-id="d8694-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d8694-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8694-118">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="d8694-118">-GatewayName</span></span>
<span data-ttu-id="d8694-119">Der Name des Daten Factory-Gateways.</span><span class="sxs-lookup"><span data-stu-id="d8694-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="d8694-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8694-120">-InputObject</span></span>
<span data-ttu-id="d8694-121">Das Data Factory-Objekt</span><span class="sxs-lookup"><span data-stu-id="d8694-121">The data factory object</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8694-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8694-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8694-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d8694-123">The resource group name.</span></span>

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

### <span data-ttu-id="d8694-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8694-124">CommonParameters</span></span>
<span data-ttu-id="d8694-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8694-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8694-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8694-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8694-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8694-127">INPUTS</span></span>

### <span data-ttu-id="d8694-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d8694-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="d8694-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d8694-129">System.String</span></span>

## <span data-ttu-id="d8694-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8694-130">OUTPUTS</span></span>

### <span data-ttu-id="d8694-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="d8694-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="d8694-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8694-132">NOTES</span></span>
* <span data-ttu-id="d8694-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="d8694-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d8694-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8694-134">RELATED LINKS</span></span>

<span data-ttu-id="d8694-135">[Neu – AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Neu – AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="d8694-135">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

