---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: 87d19475896138ee51a31694f707c1839f839ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924272"
---
# <span data-ttu-id="8afdf-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8afdf-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="8afdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8afdf-102">SYNOPSIS</span></span>
<span data-ttu-id="8afdf-103">Überprüft, ob der Name des Konfigurationsspeichers zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8afdf-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="8afdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8afdf-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8afdf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8afdf-105">DESCRIPTION</span></span>
<span data-ttu-id="8afdf-106">Überprüft, ob der Name des Konfigurationsspeichers zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8afdf-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="8afdf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8afdf-107">EXAMPLES</span></span>

### <span data-ttu-id="8afdf-108">Beispiel 1: Testen der Verfügbarkeit des Namens des App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="8afdf-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="8afdf-109">Mit diesem Befehl wird die Verfügbarkeit des Namens des App-Konfigurationsspeichers überprüft.</span><span class="sxs-lookup"><span data-stu-id="8afdf-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="8afdf-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8afdf-110">PARAMETERS</span></span>

### <span data-ttu-id="8afdf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8afdf-111">-DefaultProfile</span></span>
<span data-ttu-id="8afdf-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8afdf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afdf-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8afdf-113">-Name</span></span>
<span data-ttu-id="8afdf-114">Der Name, der auf Verfügbarkeit überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="8afdf-114">The name to check for availability.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afdf-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8afdf-115">-SubscriptionId</span></span>
<span data-ttu-id="8afdf-116">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="8afdf-116">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afdf-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8afdf-117">-Confirm</span></span>
<span data-ttu-id="8afdf-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8afdf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8afdf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8afdf-119">-WhatIf</span></span>
<span data-ttu-id="8afdf-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8afdf-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8afdf-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8afdf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8afdf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8afdf-122">CommonParameters</span></span>
<span data-ttu-id="8afdf-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8afdf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8afdf-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8afdf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8afdf-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8afdf-125">INPUTS</span></span>

## <span data-ttu-id="8afdf-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8afdf-126">OUTPUTS</span></span>

### <span data-ttu-id="8afdf-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="8afdf-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="8afdf-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8afdf-128">NOTES</span></span>

<span data-ttu-id="8afdf-129">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8afdf-129">ALIASES</span></span>

## <span data-ttu-id="8afdf-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8afdf-130">RELATED LINKS</span></span>

