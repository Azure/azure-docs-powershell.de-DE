---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479778"
---
# <span data-ttu-id="f6363-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f6363-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="f6363-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6363-102">SYNOPSIS</span></span>
<span data-ttu-id="f6363-103">Erstellt ein standortbasiertes Dienstkonto.</span><span class="sxs-lookup"><span data-stu-id="f6363-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6363-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6363-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6363-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6363-105">DESCRIPTION</span></span>
<span data-ttu-id="f6363-106">Das Cmdlet **New-AzureRmLocationBasedServicesAccount** erstellt ein Location based Services-Konto mit der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="f6363-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="f6363-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6363-107">EXAMPLES</span></span>

### <span data-ttu-id="f6363-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6363-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="f6363-109">Erstellt ein neues standortbasiertes Dienstkonto mit dem Namen "Mein Konto" in der Ressourcengruppe myresourcegroup mit der SKU S0 und einer Kategorie.</span><span class="sxs-lookup"><span data-stu-id="f6363-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="f6363-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6363-110">PARAMETERS</span></span>

### <span data-ttu-id="f6363-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6363-111">-DefaultProfile</span></span>
<span data-ttu-id="f6363-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6363-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6363-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f6363-113">-Force</span></span>
<span data-ttu-id="f6363-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="f6363-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6363-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f6363-115">-Name</span></span>
<span data-ttu-id="f6363-116">Name des standortbasierten Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="f6363-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6363-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6363-117">-ResourceGroupName</span></span>
<span data-ttu-id="f6363-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f6363-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6363-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f6363-119">-SkuName</span></span>
<span data-ttu-id="f6363-120">Standortbasierter Dienstkonto-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="f6363-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="f6363-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f6363-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6363-122">S0</span><span class="sxs-lookup"><span data-stu-id="f6363-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6363-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6363-123">-Tag</span></span>
<span data-ttu-id="f6363-124">Kontokategorien für standortbasierte Dienste</span><span class="sxs-lookup"><span data-stu-id="f6363-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6363-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6363-125">-Confirm</span></span>
<span data-ttu-id="f6363-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6363-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6363-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6363-127">-WhatIf</span></span>
<span data-ttu-id="f6363-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6363-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6363-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6363-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6363-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6363-130">CommonParameters</span></span>
<span data-ttu-id="f6363-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6363-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6363-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6363-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6363-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6363-133">INPUTS</span></span>

### <span data-ttu-id="f6363-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f6363-134">System.String</span></span>

## <span data-ttu-id="f6363-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6363-135">OUTPUTS</span></span>

### <span data-ttu-id="f6363-136">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f6363-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="f6363-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6363-137">NOTES</span></span>

<span data-ttu-id="f6363-138">Zum Erstellen eines Location based Services-Kontos muss eine Aufforderung zur Annahme von Ausdrücken beantwortet werden (siehe https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) .</span><span class="sxs-lookup"><span data-stu-id="f6363-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="f6363-139">Der Parameter-Force kann verwendet werden, um die Akzeptanz der Begriffe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f6363-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="f6363-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6363-140">RELATED LINKS</span></span>
