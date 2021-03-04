---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 84e2942037ba0d01425ca85530d33a042544dafc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939432"
---
# <span data-ttu-id="14b79-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="14b79-101">Get-AzADGroup</span></span>

## <span data-ttu-id="14b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14b79-102">SYNOPSIS</span></span>
<span data-ttu-id="14b79-103">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="14b79-103">Filters active directory groups.</span></span>

## <span data-ttu-id="14b79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14b79-104">SYNTAX</span></span>

### <span data-ttu-id="14b79-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="14b79-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="14b79-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="14b79-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="14b79-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14b79-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="14b79-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14b79-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="14b79-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14b79-109">DESCRIPTION</span></span>
<span data-ttu-id="14b79-110">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="14b79-110">Filters active directory groups.</span></span>

## <span data-ttu-id="14b79-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14b79-111">EXAMPLES</span></span>

### <span data-ttu-id="14b79-112">Beispiel 1: Auflisten aller AD-Gruppen</span><span class="sxs-lookup"><span data-stu-id="14b79-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="14b79-113">Listet alle AD-Gruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="14b79-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="14b79-114">Beispiel 2: Auflisten aller AD-Gruppen mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="14b79-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="14b79-115">Listet die ersten 100 AD-Gruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="14b79-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="14b79-116">Beispiel 3: Anzeigen der Gruppe "AD" nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="14b79-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="14b79-117">Ruft eine AD-Gruppe mit der Objekt-ID '85F89C90-780E-4AA6-9F4F-6f268D322EEEE' ab.</span><span class="sxs-lookup"><span data-stu-id="14b79-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="14b79-118">Beispiel 4: Auflisten von Gruppen nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="14b79-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="14b79-119">Listet alle AD-Gruppen auf, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="14b79-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="14b79-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="14b79-120">PARAMETERS</span></span>

### <span data-ttu-id="14b79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b79-121">-DefaultProfile</span></span>
<span data-ttu-id="14b79-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="14b79-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14b79-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="14b79-123">-DisplayName</span></span>
<span data-ttu-id="14b79-124">Der Anzeigename der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="14b79-124">The display name of the group.</span></span>

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

### <span data-ttu-id="14b79-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="14b79-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="14b79-126">Wird verwendet, um Gruppen zu suchen, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="14b79-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="14b79-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="14b79-127">-ObjectId</span></span>
<span data-ttu-id="14b79-128">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="14b79-128">Object id of the group.</span></span>

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

### <span data-ttu-id="14b79-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="14b79-129">-IncludeTotalCount</span></span>
<span data-ttu-id="14b79-130">Gibt die Anzahl der Objekte im Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="14b79-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="14b79-131">Dieser Parameter führt zurzeit nichts aus.</span><span class="sxs-lookup"><span data-stu-id="14b79-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="14b79-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="14b79-132">-Skip</span></span>
<span data-ttu-id="14b79-133">Ignoriert die ersten N-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="14b79-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="14b79-134">-First</span><span class="sxs-lookup"><span data-stu-id="14b79-134">-First</span></span>
<span data-ttu-id="14b79-135">Die maximale Anzahl von Zurücksennungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="14b79-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="14b79-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b79-136">CommonParameters</span></span>
<span data-ttu-id="14b79-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b79-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b79-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14b79-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b79-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14b79-139">INPUTS</span></span>

### <span data-ttu-id="14b79-140">System.String</span><span class="sxs-lookup"><span data-stu-id="14b79-140">System.String</span></span>

### <span data-ttu-id="14b79-141">System.Guid</span><span class="sxs-lookup"><span data-stu-id="14b79-141">System.Guid</span></span>

## <span data-ttu-id="14b79-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14b79-142">OUTPUTS</span></span>

### <span data-ttu-id="14b79-143">Microsoft.Azure.Commands.ActiveDirectory.PSDGroup</span><span class="sxs-lookup"><span data-stu-id="14b79-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="14b79-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="14b79-144">NOTES</span></span>

## <span data-ttu-id="14b79-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="14b79-145">RELATED LINKS</span></span>

[<span data-ttu-id="14b79-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="14b79-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="14b79-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14b79-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="14b79-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="14b79-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

