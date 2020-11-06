---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/reset-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 0833266bcd6e98a1d9744db2bc202bce5a01f3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480918"
---
# <span data-ttu-id="0693a-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="0693a-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="0693a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0693a-102">SYNOPSIS</span></span>
<span data-ttu-id="0693a-103">Setzt das Profil eines Server Verwaltungs Gateways zurück.</span><span class="sxs-lookup"><span data-stu-id="0693a-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0693a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0693a-104">SYNTAX</span></span>

### <span data-ttu-id="0693a-105">ByName</span><span class="sxs-lookup"><span data-stu-id="0693a-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0693a-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="0693a-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0693a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0693a-107">DESCRIPTION</span></span>
<span data-ttu-id="0693a-108">Das Cmdlet **Reset-AzureRmServerManagementGatewayProfile** setzt das Profil für ein Azure Server-Verwaltungs Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="0693a-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="0693a-109">Sie müssen das Save-AzureRmServerManagementGatewayProfile-Cmdlet verwenden, um das Profil herunterzuladen, und dann das Install-AzureRmServerManagementGatewayProfile-Cmdlet, um es zu speichern, nachdem Sie das Profil zurückgesetzt haben.</span><span class="sxs-lookup"><span data-stu-id="0693a-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="0693a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0693a-110">EXAMPLES</span></span>

## <span data-ttu-id="0693a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0693a-111">PARAMETERS</span></span>

### <span data-ttu-id="0693a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0693a-112">-DefaultProfile</span></span>
<span data-ttu-id="0693a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0693a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0693a-114">-Gateway</span><span class="sxs-lookup"><span data-stu-id="0693a-114">-Gateway</span></span>
<span data-ttu-id="0693a-115">Gibt das Gateway an, für das das Cmdlet das Profil zurücksetzt.</span><span class="sxs-lookup"><span data-stu-id="0693a-115">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="0693a-116">Kann anstelle von ResourceGoupName und Gatewayname angegeben werden</span><span class="sxs-lookup"><span data-stu-id="0693a-116">May be specified instead of ResourceGoupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0693a-117">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="0693a-117">-GatewayName</span></span>
<span data-ttu-id="0693a-118">Gibt den Namen des Gateways an, für das das Cmdlet das Profil zurücksetzt.</span><span class="sxs-lookup"><span data-stu-id="0693a-118">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0693a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0693a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0693a-120">Gibt den Namen der Ressourcengruppe an, zu der das Gateway gehört.</span><span class="sxs-lookup"><span data-stu-id="0693a-120">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0693a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0693a-121">CommonParameters</span></span>
<span data-ttu-id="0693a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0693a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0693a-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0693a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0693a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0693a-124">INPUTS</span></span>

### <span data-ttu-id="0693a-125">Gateway</span><span class="sxs-lookup"><span data-stu-id="0693a-125">Gateway</span></span>
<span data-ttu-id="0693a-126">Der Parameter "Gateway" akzeptiert den Wert vom Typ "Gateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0693a-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="0693a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0693a-127">OUTPUTS</span></span>

## <span data-ttu-id="0693a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0693a-128">NOTES</span></span>

## <span data-ttu-id="0693a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0693a-129">RELATED LINKS</span></span>

[<span data-ttu-id="0693a-130">Installieren-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="0693a-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="0693a-131">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="0693a-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


