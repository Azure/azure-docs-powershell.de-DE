---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165378"
---
# <span data-ttu-id="fb58e-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="fb58e-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="fb58e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb58e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb58e-103">Erstellt eine neue Gateway-Entität.</span><span class="sxs-lookup"><span data-stu-id="fb58e-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="fb58e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb58e-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb58e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb58e-105">DESCRIPTION</span></span>
<span data-ttu-id="fb58e-106">Das Cmdlet **New-AzApiManagementGateway** erstellt eine neue Gateway-Entität.</span><span class="sxs-lookup"><span data-stu-id="fb58e-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="fb58e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb58e-107">EXAMPLES</span></span>

### <span data-ttu-id="fb58e-108">Beispiel 1: Erstellen eines Gateways</span><span class="sxs-lookup"><span data-stu-id="fb58e-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="fb58e-109">Mit diesem Befehl wird ein Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="fb58e-109">This command creates a gateway.</span></span>

## <span data-ttu-id="fb58e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb58e-110">PARAMETERS</span></span>

### <span data-ttu-id="fb58e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fb58e-111">-Context</span></span>
<span data-ttu-id="fb58e-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fb58e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fb58e-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb58e-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb58e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb58e-114">-DefaultProfile</span></span>
<span data-ttu-id="fb58e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb58e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb58e-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb58e-116">-Description</span></span>
<span data-ttu-id="fb58e-117">Gateway-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="fb58e-117">Gateway description.</span></span>
<span data-ttu-id="fb58e-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb58e-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb58e-119">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="fb58e-119">-GatewayId</span></span>
<span data-ttu-id="fb58e-120">Bezeichner des neuen Gateways.</span><span class="sxs-lookup"><span data-stu-id="fb58e-120">Identifier of new gateway.</span></span>
<span data-ttu-id="fb58e-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb58e-121">This parameter is optional.</span></span>
<span data-ttu-id="fb58e-122">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="fb58e-122">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb58e-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="fb58e-123">-LocationData</span></span>
<span data-ttu-id="fb58e-124">Gateway-Standort.</span><span class="sxs-lookup"><span data-stu-id="fb58e-124">Gateway location.</span></span>
<span data-ttu-id="fb58e-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb58e-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb58e-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb58e-126">-Confirm</span></span>
<span data-ttu-id="fb58e-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb58e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb58e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb58e-128">-WhatIf</span></span>
<span data-ttu-id="fb58e-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb58e-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb58e-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb58e-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb58e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb58e-131">CommonParameters</span></span>
<span data-ttu-id="fb58e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb58e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb58e-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb58e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb58e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb58e-134">INPUTS</span></span>

### <span data-ttu-id="fb58e-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fb58e-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fb58e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fb58e-136">System.String</span></span>

### <span data-ttu-id="fb58e-137">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="fb58e-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="fb58e-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb58e-138">OUTPUTS</span></span>

### <span data-ttu-id="fb58e-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="fb58e-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="fb58e-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb58e-140">NOTES</span></span>

## <span data-ttu-id="fb58e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb58e-141">RELATED LINKS</span></span>
