---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ee1ac7cda19f2b37ac1313d30075aa9c620bbd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503126"
---
# <span data-ttu-id="59e48-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="59e48-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="59e48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59e48-102">SYNOPSIS</span></span>
<span data-ttu-id="59e48-103">Entfernt einen OpenID Connect-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="59e48-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59e48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59e48-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59e48-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59e48-105">DESCRIPTION</span></span>
<span data-ttu-id="59e48-106">Das Cmdlet **Remove-AzureRmApiManagementOpenIdConnectProvider** entfernt einen OpenID Connect-Anbieter für die Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="59e48-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="59e48-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59e48-107">EXAMPLES</span></span>

### <span data-ttu-id="59e48-108">Beispiel 1: Entfernen eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="59e48-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="59e48-109">Dieser Befehl entfernt einen Anbieter mit der ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="59e48-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="59e48-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59e48-110">PARAMETERS</span></span>

### <span data-ttu-id="59e48-111">-Context</span><span class="sxs-lookup"><span data-stu-id="59e48-111">-Context</span></span>
<span data-ttu-id="59e48-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="59e48-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="59e48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e48-113">-DefaultProfile</span></span>
<span data-ttu-id="59e48-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59e48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="59e48-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="59e48-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="59e48-116">Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="59e48-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="59e48-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59e48-117">-PassThru</span></span>
<span data-ttu-id="59e48-118">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="59e48-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59e48-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59e48-119">-Confirm</span></span>
<span data-ttu-id="59e48-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59e48-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e48-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59e48-121">-WhatIf</span></span>
<span data-ttu-id="59e48-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59e48-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59e48-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59e48-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e48-124">CommonParameters</span></span>
<span data-ttu-id="59e48-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59e48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e48-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59e48-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e48-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59e48-127">INPUTS</span></span>

### <span data-ttu-id="59e48-128">Keine</span><span class="sxs-lookup"><span data-stu-id="59e48-128">None</span></span>
<span data-ttu-id="59e48-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="59e48-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59e48-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59e48-130">OUTPUTS</span></span>

### <span data-ttu-id="59e48-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="59e48-131">Boolean</span></span>

## <span data-ttu-id="59e48-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="59e48-132">NOTES</span></span>

## <span data-ttu-id="59e48-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59e48-133">RELATED LINKS</span></span>

[<span data-ttu-id="59e48-134">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="59e48-134">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="59e48-135">Neu – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="59e48-135">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="59e48-136">Satz-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="59e48-136">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


