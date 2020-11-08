---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996854"
---
# <span data-ttu-id="8b9ec-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8b9ec-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="8b9ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9ec-103">Entfernt einen OpenID Connect-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="8b9ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b9ec-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b9ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="8b9ec-106">Das Cmdlet **Remove-AzApiManagementOpenIdConnectProvider** entfernt einen OpenID Connect-Anbieter für die Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="8b9ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b9ec-107">EXAMPLES</span></span>

### <span data-ttu-id="8b9ec-108">Beispiel 1: Entfernen eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="8b9ec-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="8b9ec-109">Dieser Befehl entfernt einen Anbieter mit der ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="8b9ec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b9ec-110">PARAMETERS</span></span>

### <span data-ttu-id="8b9ec-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8b9ec-111">-Context</span></span>
<span data-ttu-id="8b9ec-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8b9ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9ec-113">-DefaultProfile</span></span>
<span data-ttu-id="8b9ec-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b9ec-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="8b9ec-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="8b9ec-116">Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8b9ec-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b9ec-117">-PassThru</span></span>
<span data-ttu-id="8b9ec-118">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="8b9ec-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b9ec-119">-Confirm</span></span>
<span data-ttu-id="8b9ec-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b9ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b9ec-121">-WhatIf</span></span>
<span data-ttu-id="8b9ec-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b9ec-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b9ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9ec-124">CommonParameters</span></span>
<span data-ttu-id="8b9ec-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b9ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9ec-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b9ec-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9ec-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b9ec-127">INPUTS</span></span>

### <span data-ttu-id="8b9ec-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8b9ec-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8b9ec-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8b9ec-129">System.String</span></span>

### <span data-ttu-id="8b9ec-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="8b9ec-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8b9ec-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b9ec-131">OUTPUTS</span></span>

### <span data-ttu-id="8b9ec-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b9ec-132">System.Boolean</span></span>

## <span data-ttu-id="8b9ec-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b9ec-133">NOTES</span></span>

## <span data-ttu-id="8b9ec-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b9ec-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b9ec-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8b9ec-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8b9ec-136">Neu – AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8b9ec-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="8b9ec-137">Satz-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="8b9ec-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


