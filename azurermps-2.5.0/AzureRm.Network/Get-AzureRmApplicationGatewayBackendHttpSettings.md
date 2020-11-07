---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 366b3545e54c1465bf2eaf050a9e9199288fce5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849247"
---
# <span data-ttu-id="67264-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67264-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="67264-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67264-102">SYNOPSIS</span></span>
<span data-ttu-id="67264-103">Ruft die Back-End-HTTP-Einstellungen eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="67264-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67264-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67264-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67264-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67264-105">DESCRIPTION</span></span>
<span data-ttu-id="67264-106">Das Get-AzureRmApplicationGatewayBackendHttpSettings-Cmdlet ruft die HTTP-Back-End-Einstellungen eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="67264-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="67264-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67264-107">EXAMPLES</span></span>

### <span data-ttu-id="67264-108">Beispiel 1: Abrufen von HTTP-Back-End-Einstellungen nach Name</span><span class="sxs-lookup"><span data-stu-id="67264-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="67264-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der zweite Befehl ruft die http-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings-Variablen.</span><span class="sxs-lookup"><span data-stu-id="67264-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="67264-110">Beispiel 2: Abrufen einer Sammlung von Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="67264-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="67264-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der zweite Befehl ruft die Sammlung von http-Einstellungen für $AppGw ab und speichert die Einstellungen in der $SettingsList-Variablen.</span><span class="sxs-lookup"><span data-stu-id="67264-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="67264-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="67264-112">PARAMETERS</span></span>

### <span data-ttu-id="67264-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67264-113">-ApplicationGateway</span></span>
<span data-ttu-id="67264-114">Gibt ein Application Gateway-Objekt an, das Back-End-HTTP-Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="67264-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67264-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67264-115">-DefaultProfile</span></span>
<span data-ttu-id="67264-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67264-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67264-117">-Name</span><span class="sxs-lookup"><span data-stu-id="67264-117">-Name</span></span>
<span data-ttu-id="67264-118">Gibt den Namen der HTTP-Back-End-Einstellungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="67264-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67264-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67264-119">CommonParameters</span></span>
<span data-ttu-id="67264-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67264-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67264-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67264-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67264-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67264-122">INPUTS</span></span>

### <span data-ttu-id="67264-123">System. String</span><span class="sxs-lookup"><span data-stu-id="67264-123">System.String</span></span>

## <span data-ttu-id="67264-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67264-124">OUTPUTS</span></span>

### <span data-ttu-id="67264-125">Microsoft. Azure. Commands. Network. Models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67264-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="67264-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="67264-126">NOTES</span></span>

## <span data-ttu-id="67264-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67264-127">RELATED LINKS</span></span>

[<span data-ttu-id="67264-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67264-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="67264-129">Neu – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67264-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="67264-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67264-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="67264-131">Satz-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="67264-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

