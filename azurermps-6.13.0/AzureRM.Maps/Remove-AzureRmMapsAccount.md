---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/remove-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
ms.openlocfilehash: 9880bf574aec57796d185742b2f33b79da8f7c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479561"
---
# <span data-ttu-id="b34e9-101">Remove-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b34e9-101">Remove-AzureRmMapsAccount</span></span>

## <span data-ttu-id="b34e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b34e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b34e9-103">Löscht ein Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="b34e9-103">Deletes an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b34e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b34e9-104">SYNTAX</span></span>

### <span data-ttu-id="b34e9-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b34e9-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b34e9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b34e9-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b34e9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b34e9-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b34e9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b34e9-108">DESCRIPTION</span></span>
<span data-ttu-id="b34e9-109">Das Remove-AzureRmMapsAccount-Cmdlet löscht das angegebene Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="b34e9-109">The Remove-AzureRmMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="b34e9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b34e9-110">EXAMPLES</span></span>

### <span data-ttu-id="b34e9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b34e9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="b34e9-112">Löscht das Konto "Mein Konto" aus der Ressourcengruppe "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="b34e9-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b34e9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b34e9-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="b34e9-114">Löscht das angegebene Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="b34e9-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="b34e9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b34e9-115">PARAMETERS</span></span>

### <span data-ttu-id="b34e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34e9-116">-DefaultProfile</span></span>
<span data-ttu-id="b34e9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b34e9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b34e9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b34e9-118">-InputObject</span></span>
<span data-ttu-id="b34e9-119">Kartenkonto, das von Get-AzureRmMapsAccount umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="b34e9-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b34e9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b34e9-120">-Name</span></span>
<span data-ttu-id="b34e9-121">Ordnet den Kontonamen zu.</span><span class="sxs-lookup"><span data-stu-id="b34e9-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b34e9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b34e9-122">-PassThru</span></span>
<span data-ttu-id="b34e9-123">Gibt zurück, ob das angegebene Konto erfolgreich gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="b34e9-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="b34e9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34e9-124">-ResourceGroupName</span></span>
<span data-ttu-id="b34e9-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b34e9-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b34e9-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b34e9-126">-ResourceId</span></span>
<span data-ttu-id="b34e9-127">Maps-Konto-wiederherkunfts-Nr.</span><span class="sxs-lookup"><span data-stu-id="b34e9-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b34e9-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b34e9-128">-Confirm</span></span>
<span data-ttu-id="b34e9-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b34e9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b34e9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b34e9-130">-WhatIf</span></span>
<span data-ttu-id="b34e9-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b34e9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34e9-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b34e9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b34e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34e9-133">CommonParameters</span></span>
<span data-ttu-id="b34e9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34e9-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34e9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34e9-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b34e9-136">INPUTS</span></span>

### <span data-ttu-id="b34e9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b34e9-137">System.String</span></span>

### <span data-ttu-id="b34e9-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b34e9-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="b34e9-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b34e9-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b34e9-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b34e9-140">OUTPUTS</span></span>

### <span data-ttu-id="b34e9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b34e9-141">System.Boolean</span></span>

## <span data-ttu-id="b34e9-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="b34e9-142">NOTES</span></span>

## <span data-ttu-id="b34e9-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b34e9-143">RELATED LINKS</span></span>
