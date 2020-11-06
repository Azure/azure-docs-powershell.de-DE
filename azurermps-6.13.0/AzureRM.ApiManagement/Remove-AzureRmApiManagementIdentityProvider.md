---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d8cc54570b1282889a93c803e1216096cde35b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476338"
---
# <span data-ttu-id="6e30d-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6e30d-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="6e30d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e30d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e30d-103">Entfernt eine vorhandene Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6e30d-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e30d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e30d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e30d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e30d-105">DESCRIPTION</span></span>
<span data-ttu-id="6e30d-106">Entfernt eine vorhandene Identität Anbieterkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6e30d-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="6e30d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e30d-107">EXAMPLES</span></span>

### <span data-ttu-id="6e30d-108">Entfernt die Einstellungen des Facebook-Identitätsanbieters aus dem ApiManagement-Dienst</span><span class="sxs-lookup"><span data-stu-id="6e30d-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="6e30d-109">Löscht die Konfiguration in Bezug auf die Konfiguration des Facebook-Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="6e30d-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="6e30d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e30d-110">PARAMETERS</span></span>

### <span data-ttu-id="6e30d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6e30d-111">-Context</span></span>
<span data-ttu-id="6e30d-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6e30d-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6e30d-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e30d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6e30d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e30d-114">-DefaultProfile</span></span>
<span data-ttu-id="6e30d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e30d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e30d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e30d-116">-PassThru</span></span>
<span data-ttu-id="6e30d-117">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="6e30d-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="6e30d-118">-Typ</span><span class="sxs-lookup"><span data-stu-id="6e30d-118">-Type</span></span>
<span data-ttu-id="6e30d-119">Bezeichner eines vorhandenen Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="6e30d-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="6e30d-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6e30d-120">This parameter is required.</span></span>

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

### <span data-ttu-id="6e30d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e30d-121">-Confirm</span></span>
<span data-ttu-id="6e30d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e30d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e30d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e30d-123">-WhatIf</span></span>
<span data-ttu-id="6e30d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e30d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e30d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e30d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e30d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e30d-126">CommonParameters</span></span>
<span data-ttu-id="6e30d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e30d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e30d-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e30d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e30d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e30d-129">INPUTS</span></span>

### <span data-ttu-id="6e30d-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6e30d-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6e30d-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="6e30d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="6e30d-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="6e30d-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6e30d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e30d-133">OUTPUTS</span></span>

### <span data-ttu-id="6e30d-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e30d-134">System.Boolean</span></span>

## <span data-ttu-id="6e30d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e30d-135">NOTES</span></span>

## <span data-ttu-id="6e30d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e30d-136">RELATED LINKS</span></span>

[<span data-ttu-id="6e30d-137">Neu – AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6e30d-137">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="6e30d-138">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6e30d-138">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="6e30d-139">Satz-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6e30d-139">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

