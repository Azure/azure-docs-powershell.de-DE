---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f8bc49e4a5b4e8e7fb6285327cf4432cd0561506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820992"
---
# <span data-ttu-id="90708-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="90708-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="90708-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90708-102">SYNOPSIS</span></span>
<span data-ttu-id="90708-103">Aktualisiert die Konfiguration eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="90708-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="90708-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90708-104">SYNTAX</span></span>

```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90708-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90708-105">DESCRIPTION</span></span>
<span data-ttu-id="90708-106">Aktualisiert die Konfiguration eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="90708-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="90708-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90708-107">EXAMPLES</span></span>

### <span data-ttu-id="90708-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90708-108">Example 1</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="90708-109">Das Cmdlet aktualisiert den Client Schlüssel des Facebook-Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="90708-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="90708-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90708-110">PARAMETERS</span></span>

### <span data-ttu-id="90708-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="90708-111">-AllowedTenants</span></span>
<span data-ttu-id="90708-112">Liste der zulässigen Azure Active Directory-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="90708-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="90708-113">-ClientID</span><span class="sxs-lookup"><span data-stu-id="90708-113">-ClientId</span></span>
<span data-ttu-id="90708-114">Client-ID der Anwendung im externen Identitätsanbieter.</span><span class="sxs-lookup"><span data-stu-id="90708-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="90708-115">Es ist die APP-ID für Facebook-Anmeldung, Client-ID für Google-Anmeldung, APP-ID für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="90708-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="90708-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="90708-116">-ClientSecret</span></span>
<span data-ttu-id="90708-117">Client-Schlüssel der Anwendung im externen Identitätsanbieter, der zur Authentifizierung der Anmeldeanforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90708-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="90708-118">Beispielsweise ist es App Secret für Facebook-Anmeldung, API-Schlüssel für Google-Anmeldung, öffentlicher Schlüssel für Microsoft.</span><span class="sxs-lookup"><span data-stu-id="90708-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="90708-119">-Context</span><span class="sxs-lookup"><span data-stu-id="90708-119">-Context</span></span>
<span data-ttu-id="90708-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="90708-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="90708-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="90708-121">This parameter is required.</span></span>

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

### <span data-ttu-id="90708-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90708-122">-DefaultProfile</span></span>
<span data-ttu-id="90708-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90708-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90708-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90708-124">-PassThru</span></span>
<span data-ttu-id="90708-125">Gibt an, dass dieses Cmdlet die  **PsApiManagementIdentityProvider** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="90708-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="90708-126">-Typ</span><span class="sxs-lookup"><span data-stu-id="90708-126">-Type</span></span>
<span data-ttu-id="90708-127">Bezeichner eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="90708-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="90708-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="90708-128">This parameter is required.</span></span>

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

### <span data-ttu-id="90708-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90708-129">-Confirm</span></span>
<span data-ttu-id="90708-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90708-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90708-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90708-131">-WhatIf</span></span>
<span data-ttu-id="90708-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90708-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90708-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90708-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90708-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90708-134">CommonParameters</span></span>
<span data-ttu-id="90708-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90708-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90708-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90708-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90708-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90708-137">INPUTS</span></span>

### <span data-ttu-id="90708-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90708-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="90708-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="90708-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="90708-140">System. String</span><span class="sxs-lookup"><span data-stu-id="90708-140">System.String</span></span>

### <span data-ttu-id="90708-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="90708-141">System.String[]</span></span>

### <span data-ttu-id="90708-142">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="90708-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90708-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90708-143">OUTPUTS</span></span>

### <span data-ttu-id="90708-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="90708-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="90708-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="90708-145">NOTES</span></span>

## <span data-ttu-id="90708-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90708-146">RELATED LINKS</span></span>

[<span data-ttu-id="90708-147">Neu – AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="90708-147">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="90708-148">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="90708-148">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="90708-149">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="90708-149">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
