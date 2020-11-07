---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 880c44e3edf8a5d2c95144d2af8910e73d366192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658137"
---
# <span data-ttu-id="fe045-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fe045-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="fe045-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe045-102">SYNOPSIS</span></span>
<span data-ttu-id="fe045-103">Ändert einen OpenID Connect-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fe045-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="fe045-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe045-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe045-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe045-105">DESCRIPTION</span></span>
<span data-ttu-id="fe045-106">Das Cmdlet " **Satz-AzApiManagementOpenIdConnectProvider** " ändert einen OpenID Connect-Anbieter in Azure API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="fe045-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="fe045-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe045-107">EXAMPLES</span></span>

### <span data-ttu-id="fe045-108">Beispiel 1: Ändern des Client Geheimnisses für einen Anbieter</span><span class="sxs-lookup"><span data-stu-id="fe045-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="fe045-109">Dieser Befehl ändert den Anbieter mit der ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="fe045-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="fe045-110">Der Befehl gibt einen Client Schlüssel für den Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="fe045-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="fe045-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe045-111">PARAMETERS</span></span>

### <span data-ttu-id="fe045-112">-ClientID</span><span class="sxs-lookup"><span data-stu-id="fe045-112">-ClientId</span></span>
<span data-ttu-id="fe045-113">Gibt die Client-ID der Entwicklerkonsole an.</span><span class="sxs-lookup"><span data-stu-id="fe045-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="fe045-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="fe045-114">-ClientSecret</span></span>
<span data-ttu-id="fe045-115">Gibt den Client Schlüssel der Entwicklerkonsole an.</span><span class="sxs-lookup"><span data-stu-id="fe045-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="fe045-116">-Context</span><span class="sxs-lookup"><span data-stu-id="fe045-116">-Context</span></span>
<span data-ttu-id="fe045-117">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fe045-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fe045-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe045-118">-DefaultProfile</span></span>
<span data-ttu-id="fe045-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe045-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe045-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe045-120">-Description</span></span>
<span data-ttu-id="fe045-121">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="fe045-121">Specifies a description.</span></span>

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

### <span data-ttu-id="fe045-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="fe045-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="fe045-123">Gibt einen Metadaten-Endpunkt-URI des Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="fe045-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="fe045-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fe045-124">-Name</span></span>
<span data-ttu-id="fe045-125">Gibt einen Anzeigenamen für den Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="fe045-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="fe045-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="fe045-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="fe045-127">Gibt eine ID für den Anbieter an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fe045-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="fe045-128">Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.</span><span class="sxs-lookup"><span data-stu-id="fe045-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="fe045-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe045-129">-PassThru</span></span>
<span data-ttu-id="fe045-130">Gibt an, dass dieses Cmdlet die **PsApiManagementOpenIdConnectProvider** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fe045-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fe045-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe045-131">-Confirm</span></span>
<span data-ttu-id="fe045-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe045-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe045-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe045-133">-WhatIf</span></span>
<span data-ttu-id="fe045-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe045-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe045-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe045-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe045-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe045-136">CommonParameters</span></span>
<span data-ttu-id="fe045-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe045-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe045-138">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe045-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe045-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe045-139">INPUTS</span></span>

### <span data-ttu-id="fe045-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fe045-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fe045-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fe045-141">System.String</span></span>

### <span data-ttu-id="fe045-142">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="fe045-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fe045-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe045-143">OUTPUTS</span></span>

### <span data-ttu-id="fe045-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fe045-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="fe045-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe045-145">NOTES</span></span>

## <span data-ttu-id="fe045-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe045-146">RELATED LINKS</span></span>

[<span data-ttu-id="fe045-147">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fe045-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="fe045-148">Neu – AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fe045-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="fe045-149">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fe045-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


