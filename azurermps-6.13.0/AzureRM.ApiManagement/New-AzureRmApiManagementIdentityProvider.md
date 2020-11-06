---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d0883edb698000ae0aaff957899a03e9936e4d93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498537"
---
# <span data-ttu-id="87fd4-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="87fd4-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="87fd4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="87fd4-103">Erstellt eine neue Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="87fd4-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87fd4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87fd4-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87fd4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87fd4-105">DESCRIPTION</span></span>
<span data-ttu-id="87fd4-106">Erstellt eine neue Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="87fd4-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="87fd4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87fd4-107">EXAMPLES</span></span>

### <span data-ttu-id="87fd4-108">Beispiel 1: konfiguriert Facebook als Identitätsanbieter für Entwickler Portal-Anmeldungen</span><span class="sxs-lookup"><span data-stu-id="87fd4-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="87fd4-109">Dieser Befehl konfiguriert die Facebook-Identität als akzeptierter Identitätsanbieter im Entwickler Portal des ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="87fd4-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="87fd4-110">Dies erfordert die Eingabe der ClientID und ClientSecret der Facebook-App.</span><span class="sxs-lookup"><span data-stu-id="87fd4-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="87fd4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="87fd4-111">PARAMETERS</span></span>

### <span data-ttu-id="87fd4-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="87fd4-112">-AllowedTenants</span></span>
<span data-ttu-id="87fd4-113">Liste der zulässigen Azure Active Directory-Mandanten</span><span class="sxs-lookup"><span data-stu-id="87fd4-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="87fd4-114">-ClientID</span><span class="sxs-lookup"><span data-stu-id="87fd4-114">-ClientId</span></span>
<span data-ttu-id="87fd4-115">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="87fd4-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="87fd4-116">Es ist die APP-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, APP-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="87fd4-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="87fd4-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="87fd4-117">-ClientSecret</span></span>
<span data-ttu-id="87fd4-118">Client-Schlüssel der Anwendung im externen Identitätsanbieter, der zur Authentifizierung der Anmeldeanforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87fd4-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="87fd4-119">Beispielsweise ist es App Secret für Facebook-Anmeldung, API-Schlüssel für Google-Anmeldung, öffentlicher Schlüssel für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="87fd4-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="87fd4-120">-Context</span><span class="sxs-lookup"><span data-stu-id="87fd4-120">-Context</span></span>
<span data-ttu-id="87fd4-121">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="87fd4-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="87fd4-122">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="87fd4-122">This parameter is required.</span></span>

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

### <span data-ttu-id="87fd4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87fd4-123">-DefaultProfile</span></span>
<span data-ttu-id="87fd4-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87fd4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87fd4-125">-Typ</span><span class="sxs-lookup"><span data-stu-id="87fd4-125">-Type</span></span>
<span data-ttu-id="87fd4-126">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="87fd4-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="87fd4-127">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="87fd4-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="87fd4-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="87fd4-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="87fd4-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87fd4-129">-Confirm</span></span>
<span data-ttu-id="87fd4-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87fd4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87fd4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87fd4-131">-WhatIf</span></span>
<span data-ttu-id="87fd4-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87fd4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87fd4-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87fd4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87fd4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87fd4-134">CommonParameters</span></span>
<span data-ttu-id="87fd4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87fd4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87fd4-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87fd4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87fd4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87fd4-137">INPUTS</span></span>

### <span data-ttu-id="87fd4-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87fd4-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87fd4-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="87fd4-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="87fd4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="87fd4-140">System.String</span></span>

### <span data-ttu-id="87fd4-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="87fd4-141">System.String[]</span></span>

## <span data-ttu-id="87fd4-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87fd4-142">OUTPUTS</span></span>

### <span data-ttu-id="87fd4-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="87fd4-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="87fd4-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="87fd4-144">NOTES</span></span>

## <span data-ttu-id="87fd4-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87fd4-145">RELATED LINKS</span></span>

[<span data-ttu-id="87fd4-146">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="87fd4-146">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="87fd4-147">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="87fd4-147">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="87fd4-148">Satz-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="87fd4-148">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
