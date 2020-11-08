---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176648"
---
# <span data-ttu-id="e99cc-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e99cc-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="e99cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e99cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e99cc-103">Überprüft, ob der Name des Konfigurationsspeichers zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e99cc-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="e99cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e99cc-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e99cc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e99cc-105">DESCRIPTION</span></span>
<span data-ttu-id="e99cc-106">Überprüft, ob der Name des Konfigurationsspeichers zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e99cc-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="e99cc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e99cc-107">EXAMPLES</span></span>

### <span data-ttu-id="e99cc-108">Beispiel 1: Testen der Verfügbarkeit des App-Konfigurationsspeicher namens</span><span class="sxs-lookup"><span data-stu-id="e99cc-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="e99cc-109">Dieser Befehl testet die Verfügbarkeit des App-Konfigurationsspeicher namens.</span><span class="sxs-lookup"><span data-stu-id="e99cc-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="e99cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e99cc-110">PARAMETERS</span></span>

### <span data-ttu-id="e99cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99cc-111">-DefaultProfile</span></span>
<span data-ttu-id="e99cc-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e99cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e99cc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e99cc-113">-Name</span></span>
<span data-ttu-id="e99cc-114">Der Name, der auf Verfügbarkeit überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="e99cc-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="e99cc-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e99cc-115">-SubscriptionId</span></span>
<span data-ttu-id="e99cc-116">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e99cc-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="e99cc-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e99cc-117">-Confirm</span></span>
<span data-ttu-id="e99cc-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e99cc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e99cc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e99cc-119">-WhatIf</span></span>
<span data-ttu-id="e99cc-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e99cc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e99cc-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e99cc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e99cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99cc-122">CommonParameters</span></span>
<span data-ttu-id="e99cc-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99cc-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e99cc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99cc-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e99cc-125">INPUTS</span></span>

## <span data-ttu-id="e99cc-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e99cc-126">OUTPUTS</span></span>

### <span data-ttu-id="e99cc-127">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="e99cc-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="e99cc-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="e99cc-128">NOTES</span></span>

<span data-ttu-id="e99cc-129">Aliase</span><span class="sxs-lookup"><span data-stu-id="e99cc-129">ALIASES</span></span>

## <span data-ttu-id="e99cc-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e99cc-130">RELATED LINKS</span></span>

