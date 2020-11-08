---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 984b5ef9a1ff19142ef044e1f3c919f8fb2a3dce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178421"
---
# <span data-ttu-id="d4ca6-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="d4ca6-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="d4ca6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ca6-103">Listet Mitglieder einer Anzeigengruppe im aktuellen Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="d4ca6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4ca6-104">SYNTAX</span></span>

### <span data-ttu-id="d4ca6-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4ca6-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d4ca6-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4ca6-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d4ca6-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4ca6-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="d4ca6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4ca6-108">DESCRIPTION</span></span>
<span data-ttu-id="d4ca6-109">Listet Mitglieder einer Anzeigengruppe im aktuellen Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="d4ca6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4ca6-110">EXAMPLES</span></span>

### <span data-ttu-id="d4ca6-111">Beispiel 1: Auflisten von Mitgliedern nach Anzeigengruppen-Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="d4ca6-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="d4ca6-112">Listet Mitglieder der Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" auf.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="d4ca6-113">Beispiel 2: Auflisten von Mitgliedern nach Anzeigengruppen-Objekt-ID mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="d4ca6-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="d4ca6-114">Listet die ersten 100-Mitglieder der Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" auf.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="d4ca6-115">Beispiel 3: Auflisten von Mitgliedern nach Piping</span><span class="sxs-lookup"><span data-stu-id="d4ca6-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="d4ca6-116">Ruft die Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab und leitet Sie an das Get-AzADGroupMember-Cmdlet weiter, um alle Mitglieder in dieser Gruppe aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="d4ca6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4ca6-117">PARAMETERS</span></span>

### <span data-ttu-id="d4ca6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ca6-118">-DefaultProfile</span></span>
<span data-ttu-id="d4ca6-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d4ca6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4ca6-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="d4ca6-120">-GroupDisplayName</span></span>
<span data-ttu-id="d4ca6-121">Der Anzeigename der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-121">The display name of the group.</span></span>

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

### <span data-ttu-id="d4ca6-122">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="d4ca6-122">-GroupObject</span></span>
<span data-ttu-id="d4ca6-123">Das Gruppenobjekt, aus dem Sie Mitglieder auflisten.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-123">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="d4ca6-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="d4ca6-124">-GroupObjectId</span></span>
<span data-ttu-id="d4ca6-125">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-125">Object Id of the group.</span></span>

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

### <span data-ttu-id="d4ca6-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d4ca6-126">-IncludeTotalCount</span></span>
<span data-ttu-id="d4ca6-127">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="d4ca6-128">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="d4ca6-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="d4ca6-129">-Skip</span></span>
<span data-ttu-id="d4ca6-130">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="d4ca6-131">-First</span><span class="sxs-lookup"><span data-stu-id="d4ca6-131">-First</span></span>
<span data-ttu-id="d4ca6-132">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="d4ca6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ca6-133">CommonParameters</span></span>
<span data-ttu-id="d4ca6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4ca6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ca6-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4ca6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ca6-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4ca6-136">INPUTS</span></span>

### <span data-ttu-id="d4ca6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d4ca6-137">System.String</span></span>

### <span data-ttu-id="d4ca6-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="d4ca6-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="d4ca6-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4ca6-139">OUTPUTS</span></span>

### <span data-ttu-id="d4ca6-140">Microsoft. Azure. Commands. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="d4ca6-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="d4ca6-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4ca6-141">NOTES</span></span>

## <span data-ttu-id="d4ca6-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4ca6-142">RELATED LINKS</span></span>

[<span data-ttu-id="d4ca6-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d4ca6-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="d4ca6-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d4ca6-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

