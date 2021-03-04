---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: d351ee85c36b9f5f8493879cded058fd7220450f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936120"
---
# <span data-ttu-id="5c69b-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="5c69b-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="5c69b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c69b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c69b-103">Listet Mitglieder einer AD-Gruppe im aktuellen Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="5c69b-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="5c69b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c69b-104">SYNTAX</span></span>

### <span data-ttu-id="5c69b-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c69b-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5c69b-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c69b-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5c69b-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c69b-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5c69b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c69b-108">DESCRIPTION</span></span>
<span data-ttu-id="5c69b-109">Listet Mitglieder einer AD-Gruppe im aktuellen Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="5c69b-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="5c69b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c69b-110">EXAMPLES</span></span>

### <span data-ttu-id="5c69b-111">Beispiel 1: Auflisten von Mitgliedern nach AD-Gruppenobjekt-ID</span><span class="sxs-lookup"><span data-stu-id="5c69b-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="5c69b-112">Listet Mitglieder der GRUPPE AD mit der Objekt-ID '85F89C90-780E-4AA6-9F4F-6F268D322EEEE' auf.</span><span class="sxs-lookup"><span data-stu-id="5c69b-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5c69b-113">Beispiel 2: Auflisten von Mitgliedern nach AD-Gruppenobjekt-ID mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="5c69b-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="5c69b-114">Listet die ersten 100 Mitglieder der AD-Gruppe mit der Objekt-ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE' auf.</span><span class="sxs-lookup"><span data-stu-id="5c69b-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5c69b-115">Beispiel 3: Auflisten von Mitgliedern durch Piping</span><span class="sxs-lookup"><span data-stu-id="5c69b-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="5c69b-116">Ruft die GRUPPE AD mit der Objekt-ID '85F89C90-780E-4AA6-9F4F-6F268D322EEEE' ab und gibt sie an das Get-AzADGroupMember-Cmdlet weiter, um alle Mitglieder in dieser Gruppe auflisten zu können.</span><span class="sxs-lookup"><span data-stu-id="5c69b-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="5c69b-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5c69b-117">PARAMETERS</span></span>

### <span data-ttu-id="5c69b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c69b-118">-DefaultProfile</span></span>
<span data-ttu-id="5c69b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5c69b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c69b-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="5c69b-120">-GroupDisplayName</span></span>
<span data-ttu-id="5c69b-121">Der Anzeigename der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5c69b-121">The display name of the group.</span></span>

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

### <span data-ttu-id="5c69b-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="5c69b-122">-GroupObject</span></span>
<span data-ttu-id="5c69b-123">Das Gruppenobjekt, aus dem Sie Mitglieder auflisten möchten.</span><span class="sxs-lookup"><span data-stu-id="5c69b-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c69b-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="5c69b-124">-GroupObjectId</span></span>
<span data-ttu-id="5c69b-125">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="5c69b-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c69b-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="5c69b-126">-IncludeTotalCount</span></span>
<span data-ttu-id="5c69b-127">Gibt die Anzahl der Objekte im Datensatz an.</span><span class="sxs-lookup"><span data-stu-id="5c69b-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="5c69b-128">Dieser Parameter führt zurzeit nichts aus.</span><span class="sxs-lookup"><span data-stu-id="5c69b-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="5c69b-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="5c69b-129">-Skip</span></span>
<span data-ttu-id="5c69b-130">Ignoriert die ersten N-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="5c69b-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="5c69b-131">-First</span><span class="sxs-lookup"><span data-stu-id="5c69b-131">-First</span></span>
<span data-ttu-id="5c69b-132">Die maximale Anzahl von Zurücksennungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="5c69b-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="5c69b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c69b-133">CommonParameters</span></span>
<span data-ttu-id="5c69b-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c69b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c69b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c69b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c69b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c69b-136">INPUTS</span></span>

### <span data-ttu-id="5c69b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5c69b-137">System.String</span></span>

### <span data-ttu-id="5c69b-138">Microsoft.Azure.Commands.ActiveDirectory.PSDGroup</span><span class="sxs-lookup"><span data-stu-id="5c69b-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="5c69b-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c69b-139">OUTPUTS</span></span>

### <span data-ttu-id="5c69b-140">Microsoft.Azure.Commands.ActiveDirectory.PSDObject</span><span class="sxs-lookup"><span data-stu-id="5c69b-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="5c69b-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5c69b-141">NOTES</span></span>

## <span data-ttu-id="5c69b-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5c69b-142">RELATED LINKS</span></span>

[<span data-ttu-id="5c69b-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5c69b-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="5c69b-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5c69b-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

