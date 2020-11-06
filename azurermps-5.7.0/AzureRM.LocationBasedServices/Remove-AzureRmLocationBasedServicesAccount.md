---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500573"
---
# <span data-ttu-id="4ae62-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4ae62-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="4ae62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ae62-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae62-103">Löscht ein standortbasiertes Dienstkonto.</span><span class="sxs-lookup"><span data-stu-id="4ae62-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ae62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ae62-104">SYNTAX</span></span>

### <span data-ttu-id="4ae62-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ae62-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae62-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ae62-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae62-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ae62-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ae62-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ae62-108">DESCRIPTION</span></span>
<span data-ttu-id="4ae62-109">Das Cmdlet **Remove-AzureRmLocationBasedServicesAccount** löscht das angegebene Location based Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="4ae62-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="4ae62-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ae62-110">EXAMPLES</span></span>

### <span data-ttu-id="4ae62-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ae62-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="4ae62-112">Löscht das Konto "Mein Konto" aus der Ressourcengruppe "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="4ae62-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="4ae62-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4ae62-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="4ae62-114">Löscht das angegebene Location based Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="4ae62-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="4ae62-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ae62-115">PARAMETERS</span></span>

### <span data-ttu-id="4ae62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae62-116">-DefaultProfile</span></span>
<span data-ttu-id="4ae62-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ae62-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ae62-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ae62-118">-InputObject</span></span>
<span data-ttu-id="4ae62-119">Standortbasiertes Dienstkonto, piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="4ae62-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae62-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4ae62-120">-Name</span></span>
<span data-ttu-id="4ae62-121">Name des standortbasierten Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="4ae62-121">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae62-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae62-122">-ResourceGroupName</span></span>
<span data-ttu-id="4ae62-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ae62-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae62-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4ae62-124">-ResourceId</span></span>
<span data-ttu-id="4ae62-125">Location based Services-Konto-Resourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="4ae62-125">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae62-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ae62-126">-Confirm</span></span>
<span data-ttu-id="4ae62-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ae62-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ae62-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ae62-128">-WhatIf</span></span>
<span data-ttu-id="4ae62-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ae62-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ae62-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ae62-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ae62-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae62-131">CommonParameters</span></span>
<span data-ttu-id="4ae62-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae62-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae62-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ae62-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae62-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ae62-134">INPUTS</span></span>

### <span data-ttu-id="4ae62-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4ae62-135">System.String</span></span>

## <span data-ttu-id="4ae62-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ae62-136">OUTPUTS</span></span>

### <span data-ttu-id="4ae62-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="4ae62-137">System.Object</span></span>

## <span data-ttu-id="4ae62-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ae62-138">NOTES</span></span>

## <span data-ttu-id="4ae62-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ae62-139">RELATED LINKS</span></span>
