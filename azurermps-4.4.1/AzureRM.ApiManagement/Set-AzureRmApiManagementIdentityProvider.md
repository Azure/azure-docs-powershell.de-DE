---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 76ee402fee2e18d426875340d4eaadda2cc63042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499285"
---
# <span data-ttu-id="516db-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="516db-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="516db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="516db-102">SYNOPSIS</span></span>
<span data-ttu-id="516db-103">Aktualisiert die Konfiguration eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="516db-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="516db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="516db-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="516db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="516db-105">DESCRIPTION</span></span>
<span data-ttu-id="516db-106">Aktualisiert die Konfiguration eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="516db-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="516db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="516db-107">EXAMPLES</span></span>

### <span data-ttu-id="516db-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="516db-108">Example 1</span></span>
```
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimcontext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="516db-109">Das Cmdlet aktualisiert den Client Schlüssel des Facebook-Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="516db-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="516db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="516db-110">PARAMETERS</span></span>

### <span data-ttu-id="516db-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="516db-111">-AllowedTenants</span></span>
<span data-ttu-id="516db-112">Liste der zulässigen Azure Active Directory-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="516db-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="516db-113">-ClientID</span><span class="sxs-lookup"><span data-stu-id="516db-113">-ClientId</span></span>
<span data-ttu-id="516db-114">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="516db-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="516db-115">Es ist die APP-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, APP-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="516db-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="516db-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="516db-116">-ClientSecret</span></span>
<span data-ttu-id="516db-117">Client-Schlüssel der Anwendung im externen Identitätsanbieter, der zur Authentifizierung der Anmeldeanforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="516db-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="516db-118">Beispielsweise ist es App Secret für Facebook-Anmeldung, API-Schlüssel für Google-Anmeldung, öffentlicher Schlüssel für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="516db-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="516db-119">-Context</span><span class="sxs-lookup"><span data-stu-id="516db-119">-Context</span></span>
<span data-ttu-id="516db-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="516db-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="516db-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="516db-121">This parameter is required.</span></span>

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

### <span data-ttu-id="516db-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="516db-122">-PassThru</span></span>
<span data-ttu-id="516db-123">Gibt an, dass dieses Cmdlet die  **PsApiManagementIdentityProvider** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="516db-123">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


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

### <span data-ttu-id="516db-124">-Typ</span><span class="sxs-lookup"><span data-stu-id="516db-124">-Type</span></span>
<span data-ttu-id="516db-125">Bezeichner eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="516db-125">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="516db-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="516db-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="516db-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="516db-127">-Confirm</span></span>
<span data-ttu-id="516db-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="516db-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="516db-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="516db-129">-WhatIf</span></span>
<span data-ttu-id="516db-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="516db-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="516db-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="516db-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="516db-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="516db-132">-DefaultProfile</span></span>
<span data-ttu-id="516db-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="516db-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="516db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516db-134">CommonParameters</span></span>
<span data-ttu-id="516db-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516db-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="516db-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516db-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="516db-137">INPUTS</span></span>

## <span data-ttu-id="516db-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="516db-138">OUTPUTS</span></span>

### <span data-ttu-id="516db-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="516db-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="516db-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="516db-140">NOTES</span></span>

## <span data-ttu-id="516db-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="516db-141">RELATED LINKS</span></span>

[<span data-ttu-id="516db-142">Neu – AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="516db-142">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="516db-143">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="516db-143">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="516db-144">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="516db-144">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
