---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 764b2d091b0019cc4231828066b4067c5f054476
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146137"
---
# <span data-ttu-id="773bc-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="773bc-101">Get-AzADGroup</span></span>

## <span data-ttu-id="773bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="773bc-102">SYNOPSIS</span></span>
<span data-ttu-id="773bc-103">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="773bc-103">Filters active directory groups.</span></span>

## <span data-ttu-id="773bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="773bc-104">SYNTAX</span></span>

### <span data-ttu-id="773bc-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="773bc-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="773bc-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="773bc-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="773bc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="773bc-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="773bc-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="773bc-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="773bc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="773bc-109">DESCRIPTION</span></span>
<span data-ttu-id="773bc-110">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="773bc-110">Filters active directory groups.</span></span>

## <span data-ttu-id="773bc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="773bc-111">EXAMPLES</span></span>

### <span data-ttu-id="773bc-112">Beispiel 1: Auflisten aller AD-Gruppen</span><span class="sxs-lookup"><span data-stu-id="773bc-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="773bc-113">Listet alle AD-Gruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="773bc-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="773bc-114">Beispiel 2: Auflisten aller AD-Gruppen mithilfe von Seiten</span><span class="sxs-lookup"><span data-stu-id="773bc-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="773bc-115">Listet die ersten 100 Ad-Gruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="773bc-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="773bc-116">Beispiel 3: Gruppe "AD" nach Objekt-ID erhalten</span><span class="sxs-lookup"><span data-stu-id="773bc-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="773bc-117">Ruft eine Ad-Gruppe mit der Objekt-ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE' ab.</span><span class="sxs-lookup"><span data-stu-id="773bc-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="773bc-118">Beispiel 4: Auflisten von Gruppen nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="773bc-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="773bc-119">Enthält alle AD-Gruppen, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="773bc-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="773bc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="773bc-120">PARAMETERS</span></span>

### <span data-ttu-id="773bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="773bc-121">-DefaultProfile</span></span>
<span data-ttu-id="773bc-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="773bc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="773bc-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="773bc-123">-DisplayName</span></span>
<span data-ttu-id="773bc-124">Der Anzeigename der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="773bc-124">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773bc-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="773bc-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="773bc-126">Wird verwendet, um Gruppen zu finden, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="773bc-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="773bc-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="773bc-127">-ObjectId</span></span>
<span data-ttu-id="773bc-128">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="773bc-128">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="773bc-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="773bc-129">-IncludeTotalCount</span></span>
<span data-ttu-id="773bc-130">Meldet die Anzahl der Objekte im Datenset.</span><span class="sxs-lookup"><span data-stu-id="773bc-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="773bc-131">Derzeit führt dieser Parameter keine Anderen aus.</span><span class="sxs-lookup"><span data-stu-id="773bc-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="773bc-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="773bc-132">-Skip</span></span>
<span data-ttu-id="773bc-133">Ignoriert die ersten N-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="773bc-133">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773bc-134">-First</span><span class="sxs-lookup"><span data-stu-id="773bc-134">-First</span></span>
<span data-ttu-id="773bc-135">Die maximale Anzahl der zurückzukehrende Objekte.</span><span class="sxs-lookup"><span data-stu-id="773bc-135">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="773bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="773bc-136">CommonParameters</span></span>
<span data-ttu-id="773bc-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="773bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="773bc-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="773bc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="773bc-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="773bc-139">INPUTS</span></span>

### <span data-ttu-id="773bc-140">System.String</span><span class="sxs-lookup"><span data-stu-id="773bc-140">System.String</span></span>

### <span data-ttu-id="773bc-141">System.Guid</span><span class="sxs-lookup"><span data-stu-id="773bc-141">System.Guid</span></span>

## <span data-ttu-id="773bc-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="773bc-142">OUTPUTS</span></span>

### <span data-ttu-id="773bc-143">Microsoft.Azure.Commands.ActiveDirectory.WERDENDGroup</span><span class="sxs-lookup"><span data-stu-id="773bc-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="773bc-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="773bc-144">NOTES</span></span>

## <span data-ttu-id="773bc-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="773bc-145">RELATED LINKS</span></span>

[<span data-ttu-id="773bc-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="773bc-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="773bc-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="773bc-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="773bc-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="773bc-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

