---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361331"
---
# <span data-ttu-id="d70c4-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d70c4-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d70c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d70c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d70c4-103">Entfernt einen OpenID Connect-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="d70c4-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="d70c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d70c4-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d70c4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d70c4-105">DESCRIPTION</span></span>
<span data-ttu-id="d70c4-106">Das **Cmdlet "Remove-AzApiManagementOpenIdConnectProvider"** entfernt einen OpenID Connect-Anbieter für Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="d70c4-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="d70c4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d70c4-107">EXAMPLES</span></span>

### <span data-ttu-id="d70c4-108">Beispiel 1: Entfernen eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="d70c4-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="d70c4-109">Mit diesem Befehl wird ein Anbieter entfernt, der über die ID OICProvider01 verfügt.</span><span class="sxs-lookup"><span data-stu-id="d70c4-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="d70c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d70c4-110">PARAMETERS</span></span>

### <span data-ttu-id="d70c4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d70c4-111">-Context</span></span>
<span data-ttu-id="d70c4-112">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="d70c4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d70c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d70c4-113">-DefaultProfile</span></span>
<span data-ttu-id="d70c4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d70c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d70c4-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="d70c4-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="d70c4-116">Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="d70c4-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70c4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d70c4-117">-PassThru</span></span>
<span data-ttu-id="d70c4-118">Gibt an, dass dieses Cmdlet den Wert "$True, wenn der Vorgang erfolgreich war oder $False wurde.</span><span class="sxs-lookup"><span data-stu-id="d70c4-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70c4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d70c4-119">-Confirm</span></span>
<span data-ttu-id="d70c4-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d70c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70c4-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d70c4-121">-WhatIf</span></span>
<span data-ttu-id="d70c4-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d70c4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d70c4-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d70c4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d70c4-124">CommonParameters</span></span>
<span data-ttu-id="d70c4-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d70c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d70c4-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d70c4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d70c4-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d70c4-127">INPUTS</span></span>

### <span data-ttu-id="d70c4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d70c4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d70c4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d70c4-129">System.String</span></span>

### <span data-ttu-id="d70c4-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d70c4-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d70c4-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d70c4-131">OUTPUTS</span></span>

### <span data-ttu-id="d70c4-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d70c4-132">System.Boolean</span></span>

## <span data-ttu-id="d70c4-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d70c4-133">NOTES</span></span>

## <span data-ttu-id="d70c4-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d70c4-134">RELATED LINKS</span></span>

[<span data-ttu-id="d70c4-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d70c4-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d70c4-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d70c4-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d70c4-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d70c4-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


