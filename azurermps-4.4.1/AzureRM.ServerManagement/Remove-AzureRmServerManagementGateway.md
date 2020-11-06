---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 2bcfac139d38f0b6f7d621a7761ce01d1d3f2f45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496869"
---
# <span data-ttu-id="ba4e1-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ba4e1-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="ba4e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4e1-103">Entfernt ein Server Verwaltungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba4e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba4e1-104">SYNTAX</span></span>

### <span data-ttu-id="ba4e1-105">ByName</span><span class="sxs-lookup"><span data-stu-id="ba4e1-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba4e1-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="ba4e1-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba4e1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba4e1-107">DESCRIPTION</span></span>
<span data-ttu-id="ba4e1-108">Das Cmdlet **Remove-AzureRmServerManagementGateway** entfernt ein Azure Server-Verwaltungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="ba4e1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba4e1-109">EXAMPLES</span></span>

## <span data-ttu-id="ba4e1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba4e1-110">PARAMETERS</span></span>

### <span data-ttu-id="ba4e1-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="ba4e1-111">-Gateway</span></span>
<span data-ttu-id="ba4e1-112">Gibt das Gateway an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-112">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="ba4e1-113">Dieser Parameter kann anstelle der *ResourceGroupName* -und der *GatewayName* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-113">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4e1-114">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="ba4e1-114">-GatewayName</span></span>
<span data-ttu-id="ba4e1-115">Gibt den Namen des Gateways an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-115">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4e1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba4e1-116">-ResourceGroupName</span></span>
<span data-ttu-id="ba4e1-117">Gibt den Namen der Ressourcengruppe an, zu der das Gateway gehört.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-117">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4e1-118">-DefaultProfile</span></span>
<span data-ttu-id="ba4e1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba4e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4e1-120">CommonParameters</span></span>
<span data-ttu-id="ba4e1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4e1-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4e1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4e1-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba4e1-123">INPUTS</span></span>

### <span data-ttu-id="ba4e1-124">Gateway</span><span class="sxs-lookup"><span data-stu-id="ba4e1-124">Gateway</span></span>
<span data-ttu-id="ba4e1-125">Der Parameter "Gateway" akzeptiert den Wert vom Typ "Gateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="ba4e1-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba4e1-126">OUTPUTS</span></span>

## <span data-ttu-id="ba4e1-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba4e1-127">NOTES</span></span>
* <span data-ttu-id="ba4e1-128">Bevor Sie dieses Cmdlet verwenden können, müssen alle Knoten im Gateway entfernt werden. Andernfalls tritt für dieses Cmdlet ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ba4e1-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="ba4e1-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba4e1-129">RELATED LINKS</span></span>

[<span data-ttu-id="ba4e1-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ba4e1-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="ba4e1-131">Neu – AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ba4e1-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


