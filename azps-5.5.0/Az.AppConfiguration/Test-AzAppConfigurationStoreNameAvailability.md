---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162561"
---
# <span data-ttu-id="af66c-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="af66c-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="af66c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af66c-102">SYNOPSIS</span></span>
<span data-ttu-id="af66c-103">Überprüft, ob der Name des Konfigurationsspeichers zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="af66c-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="af66c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af66c-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af66c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af66c-105">DESCRIPTION</span></span>
<span data-ttu-id="af66c-106">Überprüft, ob der Name des Konfigurationsspeichers zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="af66c-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="af66c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af66c-107">EXAMPLES</span></span>

### <span data-ttu-id="af66c-108">Beispiel 1: Testen der Verfügbarkeit des Namens des App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="af66c-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="af66c-109">Mit diesem Befehl wird die Verfügbarkeit des Namens des App-Konfigurationsspeichers überprüft.</span><span class="sxs-lookup"><span data-stu-id="af66c-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="af66c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af66c-110">PARAMETERS</span></span>

### <span data-ttu-id="af66c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af66c-111">-DefaultProfile</span></span>
<span data-ttu-id="af66c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af66c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af66c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="af66c-113">-Name</span></span>
<span data-ttu-id="af66c-114">Der Name, um die Verfügbarkeit zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="af66c-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="af66c-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af66c-115">-SubscriptionId</span></span>
<span data-ttu-id="af66c-116">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="af66c-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="af66c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af66c-117">-Confirm</span></span>
<span data-ttu-id="af66c-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af66c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af66c-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="af66c-119">-WhatIf</span></span>
<span data-ttu-id="af66c-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af66c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af66c-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af66c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af66c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af66c-122">CommonParameters</span></span>
<span data-ttu-id="af66c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af66c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af66c-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af66c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af66c-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af66c-125">INPUTS</span></span>

## <span data-ttu-id="af66c-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af66c-126">OUTPUTS</span></span>

### <span data-ttu-id="af66c-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="af66c-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="af66c-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af66c-128">NOTES</span></span>

<span data-ttu-id="af66c-129">ALIASE</span><span class="sxs-lookup"><span data-stu-id="af66c-129">ALIASES</span></span>

## <span data-ttu-id="af66c-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af66c-130">RELATED LINKS</span></span>

