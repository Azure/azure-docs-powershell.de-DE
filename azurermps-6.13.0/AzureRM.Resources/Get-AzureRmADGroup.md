---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 8dc8188d9408c1b8e37fe44b149ceebeaf12ee4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495721"
---
# <span data-ttu-id="17dda-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="17dda-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="17dda-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17dda-102">SYNOPSIS</span></span>
<span data-ttu-id="17dda-103">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="17dda-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17dda-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17dda-104">SYNTAX</span></span>

### <span data-ttu-id="17dda-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="17dda-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="17dda-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="17dda-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="17dda-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="17dda-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="17dda-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17dda-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="17dda-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17dda-109">DESCRIPTION</span></span>
<span data-ttu-id="17dda-110">Filtert Active Directory-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="17dda-110">Filters active directory groups.</span></span>

## <span data-ttu-id="17dda-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17dda-111">EXAMPLES</span></span>

### <span data-ttu-id="17dda-112">Beispiel 1 – Auflisten aller Anzeigengruppen</span><span class="sxs-lookup"><span data-stu-id="17dda-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="17dda-113">Listet alle Anzeigengruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="17dda-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="17dda-114">Beispiel 2 – Auflisten aller Anzeigengruppen mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="17dda-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="17dda-115">Listet die ersten 100-Anzeigengruppen in einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="17dda-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="17dda-116">Beispiel 3: Abrufen einer Anzeigengruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="17dda-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="17dda-117">Ruft eine Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab.</span><span class="sxs-lookup"><span data-stu-id="17dda-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="17dda-118">Beispiel 4 – Listen Gruppen nach Suchzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="17dda-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="17dda-119">Listet alle Anzeigengruppen auf, deren Anzeigename mit "Joe" beginnt.</span><span class="sxs-lookup"><span data-stu-id="17dda-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="17dda-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="17dda-120">PARAMETERS</span></span>

### <span data-ttu-id="17dda-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17dda-121">-DefaultProfile</span></span>
<span data-ttu-id="17dda-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="17dda-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17dda-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="17dda-123">-DisplayName</span></span>
<span data-ttu-id="17dda-124">Der Anzeigename der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="17dda-124">The display name of the group.</span></span>

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

### <span data-ttu-id="17dda-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="17dda-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="17dda-126">Wird verwendet, um Gruppen zu finden, die mit der bereitgestellten Zeichenfolge beginnen.</span><span class="sxs-lookup"><span data-stu-id="17dda-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="17dda-127">-First</span><span class="sxs-lookup"><span data-stu-id="17dda-127">-First</span></span>
<span data-ttu-id="17dda-128">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17dda-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="17dda-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="17dda-129">-IncludeTotalCount</span></span>
<span data-ttu-id="17dda-130">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="17dda-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="17dda-131">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="17dda-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="17dda-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="17dda-132">-ObjectId</span></span>
<span data-ttu-id="17dda-133">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="17dda-133">Object id of the group.</span></span>

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

### <span data-ttu-id="17dda-134">-Skip</span><span class="sxs-lookup"><span data-stu-id="17dda-134">-Skip</span></span>
<span data-ttu-id="17dda-135">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="17dda-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="17dda-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17dda-136">CommonParameters</span></span>
<span data-ttu-id="17dda-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17dda-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17dda-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17dda-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17dda-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17dda-139">INPUTS</span></span>

### <span data-ttu-id="17dda-140">System. String</span><span class="sxs-lookup"><span data-stu-id="17dda-140">System.String</span></span>

### <span data-ttu-id="17dda-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="17dda-141">System.Guid</span></span>

## <span data-ttu-id="17dda-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17dda-142">OUTPUTS</span></span>

### <span data-ttu-id="17dda-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="17dda-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="17dda-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="17dda-144">NOTES</span></span>

## <span data-ttu-id="17dda-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17dda-145">RELATED LINKS</span></span>

[<span data-ttu-id="17dda-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="17dda-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="17dda-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="17dda-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="17dda-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="17dda-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

