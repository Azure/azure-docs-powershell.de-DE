---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 03d73ac28bc1869452ecc96b5c867fcbb8c372c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664565"
---
# <span data-ttu-id="39892-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="39892-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="39892-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39892-102">SYNOPSIS</span></span>
<span data-ttu-id="39892-103">Entfernt eine Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="39892-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39892-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39892-104">SYNTAX</span></span>

### <span data-ttu-id="39892-105">ResourceGroupAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39892-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39892-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39892-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39892-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39892-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39892-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39892-108">DESCRIPTION</span></span>
<span data-ttu-id="39892-109">Der **Remove-AzureRmUserAssignedIdentity** löscht die angegebene Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="39892-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="39892-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39892-110">EXAMPLES</span></span>

### <span data-ttu-id="39892-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39892-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="39892-112">Dieses Beispiel-Cmdlet löscht die Identität **id1** unter Ressourcengruppe **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="39892-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="39892-113">True</span><span class="sxs-lookup"><span data-stu-id="39892-113">True</span></span>

## <span data-ttu-id="39892-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="39892-114">PARAMETERS</span></span>

### <span data-ttu-id="39892-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39892-115">-AsJob</span></span>
<span data-ttu-id="39892-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="39892-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39892-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39892-117">-DefaultProfile</span></span>
<span data-ttu-id="39892-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39892-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39892-119">-Force</span><span class="sxs-lookup"><span data-stu-id="39892-119">-Force</span></span>
<span data-ttu-id="39892-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="39892-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="39892-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39892-121">-InputObject</span></span>
<span data-ttu-id="39892-122">Das Identity-Objekt.</span><span class="sxs-lookup"><span data-stu-id="39892-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39892-123">-Name</span><span class="sxs-lookup"><span data-stu-id="39892-123">-Name</span></span>
<span data-ttu-id="39892-124">Der Name der Identität.</span><span class="sxs-lookup"><span data-stu-id="39892-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39892-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39892-125">-ResourceGroupName</span></span>
<span data-ttu-id="39892-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="39892-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39892-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="39892-127">-ResourceId</span></span>
<span data-ttu-id="39892-128">Die Ressourcen-ID der Identität.</span><span class="sxs-lookup"><span data-stu-id="39892-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39892-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39892-129">-Confirm</span></span>
<span data-ttu-id="39892-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39892-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39892-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39892-131">-WhatIf</span></span>
<span data-ttu-id="39892-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39892-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39892-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39892-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39892-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39892-134">CommonParameters</span></span>
<span data-ttu-id="39892-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39892-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39892-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39892-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39892-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39892-137">INPUTS</span></span>

### <span data-ttu-id="39892-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="39892-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>
<span data-ttu-id="39892-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="39892-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="39892-140">System. String</span><span class="sxs-lookup"><span data-stu-id="39892-140">System.String</span></span>

## <span data-ttu-id="39892-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39892-141">OUTPUTS</span></span>

### <span data-ttu-id="39892-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39892-142">System.Boolean</span></span>

## <span data-ttu-id="39892-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="39892-143">NOTES</span></span>

## <span data-ttu-id="39892-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39892-144">RELATED LINKS</span></span>
