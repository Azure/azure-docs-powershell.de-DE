---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 470692c946175c75bf21bd613e6bbf3590854768
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662757"
---
# <span data-ttu-id="f5fd2-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f5fd2-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f5fd2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="f5fd2-103">Erstellt eine neue Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5fd2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5fd2-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5fd2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="f5fd2-106">Erstellt eine neue Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="f5fd2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5fd2-107">EXAMPLES</span></span>

### <span data-ttu-id="f5fd2-108">Beispiel 1: konfiguriert Facebook als Identitätsanbieter für Entwickler Portal-Anmeldungen</span><span class="sxs-lookup"><span data-stu-id="f5fd2-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="f5fd2-109">Dieser Befehl konfiguriert die Facebook-Identität als akzeptierter Identitätsanbieter im Entwickler Portal des ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="f5fd2-110">Dies erfordert die Eingabe der ClientID und ClientSecret der Facebook-App.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="f5fd2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5fd2-111">PARAMETERS</span></span>

### <span data-ttu-id="f5fd2-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="f5fd2-112">-AllowedTenants</span></span>
<span data-ttu-id="f5fd2-113">Liste der zulässigen Azure Active Directory-Mandanten</span><span class="sxs-lookup"><span data-stu-id="f5fd2-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd2-114">-ClientID</span><span class="sxs-lookup"><span data-stu-id="f5fd2-114">-ClientId</span></span>
<span data-ttu-id="f5fd2-115">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="f5fd2-116">Es ist die APP-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, APP-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd2-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f5fd2-117">-ClientSecret</span></span>
<span data-ttu-id="f5fd2-118">Client-Schlüssel der Anwendung im externen Identitätsanbieter, der zur Authentifizierung der Anmeldeanforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="f5fd2-119">Beispielsweise ist es App Secret für Facebook-Anmeldung, API-Schlüssel für Google-Anmeldung, öffentlicher Schlüssel für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd2-120">-Context</span><span class="sxs-lookup"><span data-stu-id="f5fd2-120">-Context</span></span>
<span data-ttu-id="f5fd2-121">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f5fd2-122">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-122">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5fd2-123">-DefaultProfile</span></span>
<span data-ttu-id="f5fd2-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f5fd2-125">-Typ</span><span class="sxs-lookup"><span data-stu-id="f5fd2-125">-Type</span></span>
<span data-ttu-id="f5fd2-126">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="f5fd2-127">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="f5fd2-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-128">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd2-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5fd2-129">-Confirm</span></span>
<span data-ttu-id="f5fd2-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5fd2-131">-WhatIf</span></span>
<span data-ttu-id="f5fd2-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5fd2-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fd2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5fd2-134">CommonParameters</span></span>
<span data-ttu-id="f5fd2-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5fd2-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5fd2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5fd2-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5fd2-137">INPUTS</span></span>

### <span data-ttu-id="f5fd2-138">Keine</span><span class="sxs-lookup"><span data-stu-id="f5fd2-138">None</span></span>
<span data-ttu-id="f5fd2-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f5fd2-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5fd2-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5fd2-140">OUTPUTS</span></span>

### <span data-ttu-id="f5fd2-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f5fd2-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f5fd2-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5fd2-142">NOTES</span></span>

## <span data-ttu-id="f5fd2-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5fd2-143">RELATED LINKS</span></span>

[<span data-ttu-id="f5fd2-144">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f5fd2-144">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="f5fd2-145">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f5fd2-145">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="f5fd2-146">Satz-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f5fd2-146">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
