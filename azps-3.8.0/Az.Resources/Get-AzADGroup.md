---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 32370d88de54b7a6004da6b66e15e08c9eca26e7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996730"
---
# <span data-ttu-id="b35e7-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="b35e7-101">Get-AzADGroup</span></span>

## <span data-ttu-id="b35e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b35e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b35e7-103">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="b35e7-103">Filters active directory groups.</span></span>

## <span data-ttu-id="b35e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b35e7-104">SYNTAX</span></span>

### <span data-ttu-id="b35e7-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b35e7-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b35e7-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b35e7-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b35e7-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b35e7-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b35e7-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b35e7-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="b35e7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b35e7-109">DESCRIPTION</span></span>
<span data-ttu-id="b35e7-110">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="b35e7-110">Filters active directory groups.</span></span>

## <span data-ttu-id="b35e7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b35e7-111">EXAMPLES</span></span>

### <span data-ttu-id="b35e7-112">Beispiel 1 – Auflisten aller Anzeigengruppen</span><span class="sxs-lookup"><span data-stu-id="b35e7-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzADGroup
```

<span data-ttu-id="b35e7-113">Listet alle Anzeigengruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="b35e7-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="b35e7-114">Beispiel 2 – Auflisten aller Anzeigengruppen mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="b35e7-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="b35e7-115">Listet die ersten 100-Anzeigengruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="b35e7-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="b35e7-116">Beispiel 3: Abrufen einer Anzeigengruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="b35e7-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="b35e7-117">Ruft eine Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab.</span><span class="sxs-lookup"><span data-stu-id="b35e7-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="b35e7-118">Beispiel 4 – Listen Gruppen nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b35e7-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="b35e7-119">Listet alle Anzeigengruppen auf, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="b35e7-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="b35e7-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="b35e7-120">PARAMETERS</span></span>

### <span data-ttu-id="b35e7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35e7-121">-DefaultProfile</span></span>
<span data-ttu-id="b35e7-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b35e7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b35e7-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b35e7-123">-DisplayName</span></span>
<span data-ttu-id="b35e7-124">Der Anzeigename der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b35e7-124">The display name of the group.</span></span>

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

### <span data-ttu-id="b35e7-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="b35e7-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="b35e7-126">Wird verwendet, um Gruppen zu finden, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="b35e7-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="b35e7-127">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="b35e7-127">-ObjectId</span></span>
<span data-ttu-id="b35e7-128">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b35e7-128">Object id of the group.</span></span>

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

### <span data-ttu-id="b35e7-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="b35e7-129">-IncludeTotalCount</span></span>
<span data-ttu-id="b35e7-130">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b35e7-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="b35e7-131">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="b35e7-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="b35e7-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="b35e7-132">-Skip</span></span>
<span data-ttu-id="b35e7-133">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="b35e7-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="b35e7-134">-First</span><span class="sxs-lookup"><span data-stu-id="b35e7-134">-First</span></span>
<span data-ttu-id="b35e7-135">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b35e7-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="b35e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35e7-136">CommonParameters</span></span>
<span data-ttu-id="b35e7-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35e7-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b35e7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35e7-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b35e7-139">INPUTS</span></span>

### <span data-ttu-id="b35e7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b35e7-140">System.String</span></span>

### <span data-ttu-id="b35e7-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b35e7-141">System.Guid</span></span>

## <span data-ttu-id="b35e7-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b35e7-142">OUTPUTS</span></span>

### <span data-ttu-id="b35e7-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="b35e7-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="b35e7-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b35e7-144">NOTES</span></span>

## <span data-ttu-id="b35e7-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b35e7-145">RELATED LINKS</span></span>

[<span data-ttu-id="b35e7-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b35e7-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="b35e7-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b35e7-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="b35e7-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="b35e7-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

