---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178092"
---
# <span data-ttu-id="0693c-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="0693c-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="0693c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0693c-102">SYNOPSIS</span></span>
<span data-ttu-id="0693c-103">Ruft das gesamte oder bestimmte API-Verwaltungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="0693c-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="0693c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0693c-104">SYNTAX</span></span>

### <span data-ttu-id="0693c-105">GetAllGateways (Standard)</span><span class="sxs-lookup"><span data-stu-id="0693c-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0693c-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="0693c-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0693c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0693c-107">DESCRIPTION</span></span>
<span data-ttu-id="0693c-108">Das Cmdlet " **Get-AzApiManagementGateway** " Ruft das gesamte oder bestimmte API-Verwaltungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="0693c-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="0693c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0693c-109">EXAMPLES</span></span>

### <span data-ttu-id="0693c-110">Beispiel 1: Abrufen aller Gateways</span><span class="sxs-lookup"><span data-stu-id="0693c-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="0693c-111">Dieser Befehl ruft alle Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="0693c-111">This command gets all gateways.</span></span>

### <span data-ttu-id="0693c-112">Beispiel 2: Abrufen eines Gateways nach ID</span><span class="sxs-lookup"><span data-stu-id="0693c-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="0693c-113">Mit diesem Befehl wird das Gateway 0123456789 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0693c-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="0693c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0693c-114">PARAMETERS</span></span>

### <span data-ttu-id="0693c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="0693c-115">-Context</span></span>
<span data-ttu-id="0693c-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0693c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0693c-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0693c-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0693c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0693c-118">-DefaultProfile</span></span>
<span data-ttu-id="0693c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0693c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0693c-120">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="0693c-120">-GatewayId</span></span>
<span data-ttu-id="0693c-121">Bezeichner eines Gateways.</span><span class="sxs-lookup"><span data-stu-id="0693c-121">Identifier of a gateway.</span></span>
<span data-ttu-id="0693c-122">Wenn angegeben, wird versucht, Gateway anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="0693c-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0693c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0693c-123">CommonParameters</span></span>
<span data-ttu-id="0693c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0693c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0693c-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0693c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0693c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0693c-126">INPUTS</span></span>

### <span data-ttu-id="0693c-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0693c-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0693c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0693c-128">System.String</span></span>

## <span data-ttu-id="0693c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0693c-129">OUTPUTS</span></span>

### <span data-ttu-id="0693c-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="0693c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="0693c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0693c-131">NOTES</span></span>

## <span data-ttu-id="0693c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0693c-132">RELATED LINKS</span></span>
