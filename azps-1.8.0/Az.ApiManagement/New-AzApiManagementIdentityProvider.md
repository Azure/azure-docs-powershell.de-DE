---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: c0730053dce60dbf556ef00f522aa463ffb26601
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661877"
---
# <span data-ttu-id="0c71d-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0c71d-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0c71d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c71d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c71d-103">Erstellt eine neue Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c71d-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="0c71d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c71d-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c71d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c71d-105">DESCRIPTION</span></span>
<span data-ttu-id="0c71d-106">Erstellt eine neue Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c71d-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="0c71d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c71d-107">EXAMPLES</span></span>

### <span data-ttu-id="0c71d-108">Beispiel 1: konfiguriert Facebook als Identitätsanbieter für Entwickler Portal-Anmeldungen</span><span class="sxs-lookup"><span data-stu-id="0c71d-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="0c71d-109">Dieser Befehl konfiguriert die Facebook-Identität als akzeptierter Identitätsanbieter im Entwickler Portal des ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="0c71d-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="0c71d-110">Dies erfordert die Eingabe der ClientID und ClientSecret der Facebook-App.</span><span class="sxs-lookup"><span data-stu-id="0c71d-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="0c71d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c71d-111">PARAMETERS</span></span>

### <span data-ttu-id="0c71d-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="0c71d-112">-AllowedTenants</span></span>
<span data-ttu-id="0c71d-113">Liste der zulässigen Azure Active Directory-Mandanten</span><span class="sxs-lookup"><span data-stu-id="0c71d-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c71d-114">-ClientID</span><span class="sxs-lookup"><span data-stu-id="0c71d-114">-ClientId</span></span>
<span data-ttu-id="0c71d-115">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="0c71d-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="0c71d-116">Es ist die APP-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, APP-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0c71d-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="0c71d-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="0c71d-117">-ClientSecret</span></span>
<span data-ttu-id="0c71d-118">Client-Schlüssel der Anwendung im externen Identitätsanbieter, der zur Authentifizierung der Anmeldeanforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c71d-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="0c71d-119">Beispielsweise ist es App Secret für Facebook-Anmeldung, API-Schlüssel für Google-Anmeldung, öffentlicher Schlüssel für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0c71d-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="0c71d-120">-Context</span><span class="sxs-lookup"><span data-stu-id="0c71d-120">-Context</span></span>
<span data-ttu-id="0c71d-121">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0c71d-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0c71d-122">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0c71d-122">This parameter is required.</span></span>

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

### <span data-ttu-id="0c71d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c71d-123">-DefaultProfile</span></span>
<span data-ttu-id="0c71d-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c71d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c71d-125">-Typ</span><span class="sxs-lookup"><span data-stu-id="0c71d-125">-Type</span></span>
<span data-ttu-id="0c71d-126">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="0c71d-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="0c71d-127">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="0c71d-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="0c71d-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0c71d-128">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c71d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0c71d-129">-Confirm</span></span>
<span data-ttu-id="0c71d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c71d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c71d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c71d-131">-WhatIf</span></span>
<span data-ttu-id="0c71d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c71d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c71d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c71d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c71d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c71d-134">CommonParameters</span></span>
<span data-ttu-id="0c71d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c71d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c71d-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c71d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c71d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c71d-137">INPUTS</span></span>

### <span data-ttu-id="0c71d-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0c71d-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0c71d-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="0c71d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="0c71d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0c71d-140">System.String</span></span>

### <span data-ttu-id="0c71d-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="0c71d-141">System.String[]</span></span>

## <span data-ttu-id="0c71d-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c71d-142">OUTPUTS</span></span>

### <span data-ttu-id="0c71d-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0c71d-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0c71d-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c71d-144">NOTES</span></span>

## <span data-ttu-id="0c71d-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c71d-145">RELATED LINKS</span></span>

[<span data-ttu-id="0c71d-146">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0c71d-146">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="0c71d-147">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0c71d-147">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="0c71d-148">Satz-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0c71d-148">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
