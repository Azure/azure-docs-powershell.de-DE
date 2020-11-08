---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009225"
---
# <span data-ttu-id="b477d-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b477d-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="b477d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b477d-102">SYNOPSIS</span></span>
<span data-ttu-id="b477d-103">Erstellt ein Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="b477d-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="b477d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b477d-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b477d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b477d-105">DESCRIPTION</span></span>
<span data-ttu-id="b477d-106">Das New-AzMapsAccount-Cmdlet erstellt ein Azure Maps-Konto mit der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="b477d-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="b477d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b477d-107">EXAMPLES</span></span>

### <span data-ttu-id="b477d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b477d-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="b477d-109">Erstellt ein neues Azure Maps-Konto mit dem Namen "Mein Konto" in der Ressourcengruppe myresourcegroup mit der SKU S0 und einer Kategorie.</span><span class="sxs-lookup"><span data-stu-id="b477d-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="b477d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b477d-110">PARAMETERS</span></span>

### <span data-ttu-id="b477d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b477d-111">-DefaultProfile</span></span>
<span data-ttu-id="b477d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b477d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b477d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b477d-113">-Force</span></span>
<span data-ttu-id="b477d-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="b477d-114">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b477d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b477d-115">-Name</span></span>
<span data-ttu-id="b477d-116">Ordnet den Kontonamen zu.</span><span class="sxs-lookup"><span data-stu-id="b477d-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b477d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b477d-117">-ResourceGroupName</span></span>
<span data-ttu-id="b477d-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b477d-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b477d-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b477d-119">-SkuName</span></span>
<span data-ttu-id="b477d-120">Ordnet den SKU-Namen des Kontos zu.</span><span class="sxs-lookup"><span data-stu-id="b477d-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b477d-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="b477d-121">-Tag</span></span>
<span data-ttu-id="b477d-122">Ordnet Kontokategorien zu.</span><span class="sxs-lookup"><span data-stu-id="b477d-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b477d-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b477d-123">-Confirm</span></span>
<span data-ttu-id="b477d-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b477d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b477d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b477d-125">-WhatIf</span></span>
<span data-ttu-id="b477d-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b477d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b477d-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b477d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b477d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b477d-128">CommonParameters</span></span>
<span data-ttu-id="b477d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b477d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b477d-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b477d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b477d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b477d-131">INPUTS</span></span>

### <span data-ttu-id="b477d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b477d-132">System.String</span></span>

## <span data-ttu-id="b477d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b477d-133">OUTPUTS</span></span>

### <span data-ttu-id="b477d-134">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b477d-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="b477d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b477d-135">NOTES</span></span>

## <span data-ttu-id="b477d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b477d-136">RELATED LINKS</span></span>
