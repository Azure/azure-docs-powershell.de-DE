---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177553"
---
# <span data-ttu-id="ccbb7-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ccbb7-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="ccbb7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbb7-103">Entfernt eine Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="ccbb7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccbb7-104">SYNTAX</span></span>

### <span data-ttu-id="ccbb7-105">ResourceGroupAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ccbb7-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccbb7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccbb7-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccbb7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccbb7-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccbb7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccbb7-108">DESCRIPTION</span></span>
<span data-ttu-id="ccbb7-109">Der **Remove-AzUserAssignedIdentity** löscht die angegebene Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="ccbb7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccbb7-110">EXAMPLES</span></span>

### <span data-ttu-id="ccbb7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ccbb7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="ccbb7-112">Dieses Beispiel-Cmdlet löscht die Identität **id1** unter Ressourcengruppe **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="ccbb7-113">True</span><span class="sxs-lookup"><span data-stu-id="ccbb7-113">True</span></span>

## <span data-ttu-id="ccbb7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccbb7-114">PARAMETERS</span></span>

### <span data-ttu-id="ccbb7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccbb7-115">-AsJob</span></span>
<span data-ttu-id="ccbb7-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ccbb7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccbb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbb7-117">-DefaultProfile</span></span>
<span data-ttu-id="ccbb7-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccbb7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ccbb7-119">-Force</span></span>
<span data-ttu-id="ccbb7-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="ccbb7-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="ccbb7-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ccbb7-121">-InputObject</span></span>
<span data-ttu-id="ccbb7-122">Das Identity-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-122">The Identity object.</span></span>

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

### <span data-ttu-id="ccbb7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ccbb7-123">-Name</span></span>
<span data-ttu-id="ccbb7-124">Der Name der Identität.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-124">The Identity name.</span></span>

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

### <span data-ttu-id="ccbb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccbb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="ccbb7-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-126">The resource group name.</span></span>

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

### <span data-ttu-id="ccbb7-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ccbb7-127">-ResourceId</span></span>
<span data-ttu-id="ccbb7-128">Die Ressourcen-ID der Identität.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="ccbb7-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ccbb7-129">-Confirm</span></span>
<span data-ttu-id="ccbb7-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccbb7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccbb7-131">-WhatIf</span></span>
<span data-ttu-id="ccbb7-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccbb7-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccbb7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbb7-134">CommonParameters</span></span>
<span data-ttu-id="ccbb7-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbb7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbb7-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbb7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbb7-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccbb7-137">INPUTS</span></span>

### <span data-ttu-id="ccbb7-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ccbb7-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="ccbb7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ccbb7-139">System.String</span></span>

## <span data-ttu-id="ccbb7-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccbb7-140">OUTPUTS</span></span>

### <span data-ttu-id="ccbb7-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ccbb7-141">System.Boolean</span></span>

## <span data-ttu-id="ccbb7-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccbb7-142">NOTES</span></span>

## <span data-ttu-id="ccbb7-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccbb7-143">RELATED LINKS</span></span>
