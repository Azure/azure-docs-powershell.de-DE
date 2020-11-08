---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: e15e6757d6a4d0f6e84a9580877deecdeede94ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008749"
---
# <span data-ttu-id="b2916-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b2916-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b2916-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2916-102">SYNOPSIS</span></span>
<span data-ttu-id="b2916-103">Entfernt eine vorhandene Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2916-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="b2916-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2916-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2916-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2916-105">DESCRIPTION</span></span>
<span data-ttu-id="b2916-106">Entfernt eine vorhandene Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2916-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="b2916-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2916-107">EXAMPLES</span></span>

### <span data-ttu-id="b2916-108">Beispiel 1: entfernt die Einstellungen des Facebook-Identitätsanbieters aus dem ApiManagement-Dienst</span><span class="sxs-lookup"><span data-stu-id="b2916-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="b2916-109">Löscht die Konfiguration in Bezug auf die Konfiguration des Facebook-Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="b2916-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="b2916-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2916-110">PARAMETERS</span></span>

### <span data-ttu-id="b2916-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b2916-111">-Context</span></span>
<span data-ttu-id="b2916-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b2916-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b2916-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b2916-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b2916-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2916-114">-DefaultProfile</span></span>
<span data-ttu-id="b2916-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2916-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2916-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2916-116">-PassThru</span></span>
<span data-ttu-id="b2916-117">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="b2916-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="b2916-118">-Typ</span><span class="sxs-lookup"><span data-stu-id="b2916-118">-Type</span></span>
<span data-ttu-id="b2916-119">Bezeichner eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="b2916-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="b2916-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b2916-120">This parameter is required.</span></span>

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

### <span data-ttu-id="b2916-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2916-121">-Confirm</span></span>
<span data-ttu-id="b2916-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2916-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2916-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2916-123">-WhatIf</span></span>
<span data-ttu-id="b2916-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2916-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2916-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2916-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2916-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2916-126">CommonParameters</span></span>
<span data-ttu-id="b2916-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2916-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2916-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2916-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2916-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2916-129">INPUTS</span></span>

### <span data-ttu-id="b2916-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b2916-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b2916-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="b2916-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="b2916-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="b2916-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b2916-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2916-133">OUTPUTS</span></span>

### <span data-ttu-id="b2916-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2916-134">System.Boolean</span></span>

## <span data-ttu-id="b2916-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2916-135">NOTES</span></span>

## <span data-ttu-id="b2916-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2916-136">RELATED LINKS</span></span>

[<span data-ttu-id="b2916-137">Neu – AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b2916-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b2916-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b2916-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="b2916-139">Satz-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b2916-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

