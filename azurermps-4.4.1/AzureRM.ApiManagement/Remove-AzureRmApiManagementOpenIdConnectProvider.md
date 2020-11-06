---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 686b988ef5bf62e5eed7e4f8fae94f6b29b1b4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479993"
---
# <span data-ttu-id="b7b28-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b7b28-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b7b28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7b28-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b28-103">Entfernt einen OpenID Connect-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="b7b28-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7b28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7b28-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7b28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7b28-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b28-106">Das Cmdlet **Remove-AzureRmApiManagementOpenIdConnectProvider** entfernt einen OpenID Connect-Anbieter für die Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="b7b28-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="b7b28-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7b28-107">EXAMPLES</span></span>

### <span data-ttu-id="b7b28-108">Beispiel 1: Entfernen eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="b7b28-108">Example 1: Remove a provider</span></span>
```
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="b7b28-109">Dieser Befehl entfernt einen Anbieter mit der ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="b7b28-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="b7b28-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7b28-110">PARAMETERS</span></span>

### <span data-ttu-id="b7b28-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b7b28-111">-Context</span></span>
<span data-ttu-id="b7b28-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b7b28-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b7b28-113">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b7b28-113">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b7b28-114">Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="b7b28-114">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b7b28-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7b28-115">-PassThru</span></span>
<span data-ttu-id="b7b28-116">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="b7b28-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="b7b28-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7b28-117">-Confirm</span></span>
<span data-ttu-id="b7b28-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7b28-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7b28-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b28-119">-WhatIf</span></span>
<span data-ttu-id="b7b28-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7b28-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7b28-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7b28-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7b28-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b28-122">-DefaultProfile</span></span>
<span data-ttu-id="b7b28-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7b28-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7b28-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b28-124">CommonParameters</span></span>
<span data-ttu-id="b7b28-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b28-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b28-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b28-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b28-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7b28-127">INPUTS</span></span>

## <span data-ttu-id="b7b28-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7b28-128">OUTPUTS</span></span>

### <span data-ttu-id="b7b28-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="b7b28-129">Boolean</span></span>

## <span data-ttu-id="b7b28-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7b28-130">NOTES</span></span>

## <span data-ttu-id="b7b28-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7b28-131">RELATED LINKS</span></span>

[<span data-ttu-id="b7b28-132">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b7b28-132">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b7b28-133">Neu – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b7b28-133">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b7b28-134">Satz-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b7b28-134">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


