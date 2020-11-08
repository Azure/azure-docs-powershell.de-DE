---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174664"
---
# <span data-ttu-id="1c5c4-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1c5c4-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="1c5c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5c4-103">Löscht ein Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="1c5c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c5c4-104">SYNTAX</span></span>

### <span data-ttu-id="1c5c4-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c5c4-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c5c4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c5c4-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c5c4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c5c4-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c5c4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c5c4-108">DESCRIPTION</span></span>
<span data-ttu-id="1c5c4-109">Das Remove-AzMapsAccount-Cmdlet löscht das angegebene Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="1c5c4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c5c4-110">EXAMPLES</span></span>

### <span data-ttu-id="1c5c4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c5c4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="1c5c4-112">Löscht das Konto "Mein Konto" aus der Ressourcengruppe "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="1c5c4-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="1c5c4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1c5c4-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="1c5c4-114">Löscht das angegebene Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="1c5c4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c5c4-115">PARAMETERS</span></span>

### <span data-ttu-id="1c5c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5c4-116">-DefaultProfile</span></span>
<span data-ttu-id="1c5c4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c5c4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1c5c4-118">-InputObject</span></span>
<span data-ttu-id="1c5c4-119">Kartenkonto, das von Get-AzMapsAccount umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="1c5c4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1c5c4-120">-Name</span></span>
<span data-ttu-id="1c5c4-121">Ordnet den Kontonamen zu.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="1c5c4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c5c4-122">-PassThru</span></span>
<span data-ttu-id="1c5c4-123">Gibt zurück, ob das angegebene Konto erfolgreich gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="1c5c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c5c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c5c4-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1c5c4-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1c5c4-126">-ResourceId</span></span>
<span data-ttu-id="1c5c4-127">Maps-Konto-wiederherkunfts-Nr.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="1c5c4-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c5c4-128">-Confirm</span></span>
<span data-ttu-id="1c5c4-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c5c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c5c4-130">-WhatIf</span></span>
<span data-ttu-id="1c5c4-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c5c4-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c5c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5c4-133">CommonParameters</span></span>
<span data-ttu-id="1c5c4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c5c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5c4-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c5c4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5c4-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c5c4-136">INPUTS</span></span>

### <span data-ttu-id="1c5c4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1c5c4-137">System.String</span></span>

### <span data-ttu-id="1c5c4-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1c5c4-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="1c5c4-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c5c4-139">OUTPUTS</span></span>

### <span data-ttu-id="1c5c4-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c5c4-140">System.Boolean</span></span>

## <span data-ttu-id="1c5c4-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c5c4-141">NOTES</span></span>

## <span data-ttu-id="1c5c4-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c5c4-142">RELATED LINKS</span></span>
