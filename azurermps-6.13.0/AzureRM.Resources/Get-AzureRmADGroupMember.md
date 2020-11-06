---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: ffc04a6b1560845a0c29db4d000270fe91aa8ff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505729"
---
# <span data-ttu-id="0444f-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="0444f-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="0444f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0444f-102">SYNOPSIS</span></span>
<span data-ttu-id="0444f-103">Listet Mitglieder einer Anzeigengruppe im aktuellen Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="0444f-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0444f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0444f-104">SYNTAX</span></span>

### <span data-ttu-id="0444f-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0444f-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0444f-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0444f-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0444f-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0444f-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="0444f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0444f-108">DESCRIPTION</span></span>
<span data-ttu-id="0444f-109">Listet Mitglieder einer Anzeigengruppe im aktuellen Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="0444f-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="0444f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0444f-110">EXAMPLES</span></span>

### <span data-ttu-id="0444f-111">Beispiel 1: Auflisten von Mitgliedern nach Anzeigengruppen-Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="0444f-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="0444f-112">Listet Mitglieder der Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" auf.</span><span class="sxs-lookup"><span data-stu-id="0444f-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="0444f-113">Beispiel 2: Auflisten von Mitgliedern nach Anzeigengruppen-Objekt-ID mithilfe von Paging</span><span class="sxs-lookup"><span data-stu-id="0444f-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="0444f-114">Listet die ersten 100-Mitglieder der Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" auf.</span><span class="sxs-lookup"><span data-stu-id="0444f-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="0444f-115">Beispiel 3: Auflisten von Mitgliedern nach Piping</span><span class="sxs-lookup"><span data-stu-id="0444f-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="0444f-116">Ruft die Anzeigengruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" ab und leitet Sie an das Get-AzureRmADGroupMember-Cmdlet weiter, um alle Mitglieder in dieser Gruppe aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="0444f-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="0444f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0444f-117">PARAMETERS</span></span>

### <span data-ttu-id="0444f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0444f-118">-DefaultProfile</span></span>
<span data-ttu-id="0444f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0444f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0444f-120">-First</span><span class="sxs-lookup"><span data-stu-id="0444f-120">-First</span></span>
<span data-ttu-id="0444f-121">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0444f-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="0444f-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="0444f-122">-GroupDisplayName</span></span>
<span data-ttu-id="0444f-123">Der Anzeigename der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="0444f-123">The display name of the group.</span></span>

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

### <span data-ttu-id="0444f-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="0444f-124">-GroupObject</span></span>
<span data-ttu-id="0444f-125">Das Gruppenobjekt, aus dem Sie Mitglieder auflisten.</span><span class="sxs-lookup"><span data-stu-id="0444f-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0444f-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="0444f-126">-GroupObjectId</span></span>
<span data-ttu-id="0444f-127">Objekt-ID der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="0444f-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0444f-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="0444f-128">-IncludeTotalCount</span></span>
<span data-ttu-id="0444f-129">Gibt die Anzahl der Objekte in der Datengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0444f-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="0444f-130">Derzeit hat dieser Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="0444f-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="0444f-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="0444f-131">-Skip</span></span>
<span data-ttu-id="0444f-132">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="0444f-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="0444f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0444f-133">CommonParameters</span></span>
<span data-ttu-id="0444f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0444f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0444f-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0444f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0444f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0444f-136">INPUTS</span></span>

### <span data-ttu-id="0444f-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0444f-137">System.Guid</span></span>

### <span data-ttu-id="0444f-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="0444f-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="0444f-139">Parameter: groupobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0444f-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="0444f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0444f-140">OUTPUTS</span></span>

### <span data-ttu-id="0444f-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="0444f-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="0444f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="0444f-142">NOTES</span></span>

## <span data-ttu-id="0444f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0444f-143">RELATED LINKS</span></span>

[<span data-ttu-id="0444f-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0444f-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="0444f-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0444f-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

