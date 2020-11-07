---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: 9ddc9658d6d18cc7a08df33f1f976521656c9234
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849051"
---
# <span data-ttu-id="3aaa2-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="3aaa2-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="3aaa2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3aaa2-102">SYNOPSIS</span></span>
<span data-ttu-id="3aaa2-103">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aaa2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aaa2-104">SYNTAX</span></span>

### <span data-ttu-id="3aaa2-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3aaa2-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3aaa2-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aaa2-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3aaa2-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aaa2-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3aaa2-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aaa2-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="3aaa2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3aaa2-109">DESCRIPTION</span></span>
<span data-ttu-id="3aaa2-110">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-110">Filters active directory groups.</span></span>

## <span data-ttu-id="3aaa2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3aaa2-111">EXAMPLES</span></span>

### <span data-ttu-id="3aaa2-112">Beispiel 1 – Auflisten aller Anzeigengruppen</span><span class="sxs-lookup"><span data-stu-id="3aaa2-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="3aaa2-113">Listet alle Anzeigengruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="3aaa2-114">Beispiel 2 – Auflisten aller Anzeigengruppen mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="3aaa2-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="3aaa2-115">Listet die ersten 100-Anzeigengruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="3aaa2-116">Beispiel 3: Abrufen einer Anzeigengruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="3aaa2-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="3aaa2-117">Ruft eine Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="3aaa2-118">Beispiel 4 – Listen Gruppen nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3aaa2-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="3aaa2-119">Listet alle Anzeigengruppen auf, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="3aaa2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="3aaa2-120">PARAMETERS</span></span>

### <span data-ttu-id="3aaa2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aaa2-121">-DefaultProfile</span></span>
<span data-ttu-id="3aaa2-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3aaa2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3aaa2-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3aaa2-123">-DisplayName</span></span>
<span data-ttu-id="3aaa2-124">Der Anzeigename der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-124">The display name of the group.</span></span>

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

### <span data-ttu-id="3aaa2-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="3aaa2-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="3aaa2-126">Wird verwendet, um Gruppen zu finden, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="3aaa2-127">-First</span><span class="sxs-lookup"><span data-stu-id="3aaa2-127">-First</span></span>
<span data-ttu-id="3aaa2-128">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="3aaa2-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="3aaa2-129">-IncludeTotalCount</span></span>
<span data-ttu-id="3aaa2-130">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="3aaa2-131">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="3aaa2-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="3aaa2-132">-ObjectId</span></span>
<span data-ttu-id="3aaa2-133">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-133">Object id of the group.</span></span>

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

### <span data-ttu-id="3aaa2-134">-Skip</span><span class="sxs-lookup"><span data-stu-id="3aaa2-134">-Skip</span></span>
<span data-ttu-id="3aaa2-135">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="3aaa2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aaa2-136">CommonParameters</span></span>
<span data-ttu-id="3aaa2-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aaa2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aaa2-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aaa2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aaa2-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3aaa2-139">INPUTS</span></span>

### <span data-ttu-id="3aaa2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3aaa2-140">System.String</span></span>

### <span data-ttu-id="3aaa2-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3aaa2-141">System.Guid</span></span>

## <span data-ttu-id="3aaa2-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3aaa2-142">OUTPUTS</span></span>

### <span data-ttu-id="3aaa2-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="3aaa2-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="3aaa2-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="3aaa2-144">NOTES</span></span>

## <span data-ttu-id="3aaa2-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3aaa2-145">RELATED LINKS</span></span>

[<span data-ttu-id="3aaa2-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="3aaa2-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="3aaa2-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3aaa2-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="3aaa2-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="3aaa2-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

