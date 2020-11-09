---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 764b2d091b0019cc4231828066b4067c5f054476
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300567"
---
# <span data-ttu-id="cc6cd-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="cc6cd-101">Get-AzADGroup</span></span>

## <span data-ttu-id="cc6cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6cd-103">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-103">Filters active directory groups.</span></span>

## <span data-ttu-id="cc6cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc6cd-104">SYNTAX</span></span>

### <span data-ttu-id="cc6cd-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc6cd-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc6cd-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc6cd-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc6cd-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc6cd-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="cc6cd-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc6cd-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="cc6cd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc6cd-109">DESCRIPTION</span></span>
<span data-ttu-id="cc6cd-110">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-110">Filters active directory groups.</span></span>

## <span data-ttu-id="cc6cd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc6cd-111">EXAMPLES</span></span>

### <span data-ttu-id="cc6cd-112">Beispiel 1: Auflisten aller Anzeigengruppen</span><span class="sxs-lookup"><span data-stu-id="cc6cd-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="cc6cd-113">Listet alle Anzeigengruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="cc6cd-114">Beispiel 2: Auflisten aller Anzeigengruppen mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="cc6cd-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="cc6cd-115">Listet die ersten 100-Anzeigengruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="cc6cd-116">Beispiel 3: Abrufen der Anzeigengruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="cc6cd-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="cc6cd-117">Ruft eine Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="cc6cd-118">Beispiel 4: Auflisten von Gruppen nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cc6cd-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="cc6cd-119">Listet alle Anzeigengruppen auf, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="cc6cd-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc6cd-120">PARAMETERS</span></span>

### <span data-ttu-id="cc6cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6cd-121">-DefaultProfile</span></span>
<span data-ttu-id="cc6cd-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cc6cd-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc6cd-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cc6cd-123">-DisplayName</span></span>
<span data-ttu-id="cc6cd-124">Der Anzeigename der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-124">The display name of the group.</span></span>

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

### <span data-ttu-id="cc6cd-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="cc6cd-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="cc6cd-126">Wird verwendet, um Gruppen zu finden, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="cc6cd-127">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="cc6cd-127">-ObjectId</span></span>
<span data-ttu-id="cc6cd-128">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-128">Object id of the group.</span></span>

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

### <span data-ttu-id="cc6cd-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="cc6cd-129">-IncludeTotalCount</span></span>
<span data-ttu-id="cc6cd-130">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="cc6cd-131">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="cc6cd-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="cc6cd-132">-Skip</span></span>
<span data-ttu-id="cc6cd-133">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="cc6cd-134">-First</span><span class="sxs-lookup"><span data-stu-id="cc6cd-134">-First</span></span>
<span data-ttu-id="cc6cd-135">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="cc6cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6cd-136">CommonParameters</span></span>
<span data-ttu-id="cc6cd-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc6cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6cd-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc6cd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6cd-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc6cd-139">INPUTS</span></span>

### <span data-ttu-id="cc6cd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cc6cd-140">System.String</span></span>

### <span data-ttu-id="cc6cd-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cc6cd-141">System.Guid</span></span>

## <span data-ttu-id="cc6cd-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc6cd-142">OUTPUTS</span></span>

### <span data-ttu-id="cc6cd-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="cc6cd-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="cc6cd-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc6cd-144">NOTES</span></span>

## <span data-ttu-id="cc6cd-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc6cd-145">RELATED LINKS</span></span>

[<span data-ttu-id="cc6cd-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="cc6cd-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="cc6cd-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cc6cd-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="cc6cd-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="cc6cd-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

