---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: 511d028c8307e53884cfa16472021fc59760b929
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848087"
---
# <span data-ttu-id="3311e-101">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="3311e-101">Remove-AzureRmADGroup</span></span>

## <span data-ttu-id="3311e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3311e-102">SYNOPSIS</span></span>
<span data-ttu-id="3311e-103">Löscht eine Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3311e-103">Deletes an active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3311e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3311e-104">SYNTAX</span></span>

### <span data-ttu-id="3311e-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3311e-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3311e-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3311e-106">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3311e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3311e-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3311e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3311e-108">DESCRIPTION</span></span>
<span data-ttu-id="3311e-109">Löscht eine Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3311e-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="3311e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3311e-110">EXAMPLES</span></span>

### <span data-ttu-id="3311e-111">Beispiel 1: Entfernen einer Gruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="3311e-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="3311e-112">Entfernt die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="3311e-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="3311e-113">Beispiel 2 – Entfernen einer Gruppe nach Piping</span><span class="sxs-lookup"><span data-stu-id="3311e-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroup
```

<span data-ttu-id="3311e-114">Ruft die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" und Pipes ab, die Remove-AzureRmADGroup, um die Gruppe aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3311e-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzureRmADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="3311e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3311e-115">PARAMETERS</span></span>

### <span data-ttu-id="3311e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3311e-116">-DefaultProfile</span></span>
<span data-ttu-id="3311e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3311e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3311e-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3311e-118">-DisplayName</span></span>
<span data-ttu-id="3311e-119">Der Anzeigename der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3311e-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="3311e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3311e-120">-Force</span></span>
<span data-ttu-id="3311e-121">Wenn angegeben, wird keine Bestätigung zum Löschen der Gruppe verlangt.</span><span class="sxs-lookup"><span data-stu-id="3311e-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3311e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3311e-122">-InputObject</span></span>
<span data-ttu-id="3311e-123">Die Objektdarstellung der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3311e-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3311e-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="3311e-124">-ObjectId</span></span>
<span data-ttu-id="3311e-125">Die Objekt-ID der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3311e-125">The object id of the group to be removed.</span></span>

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

### <span data-ttu-id="3311e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3311e-126">-PassThru</span></span>
<span data-ttu-id="3311e-127">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3311e-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3311e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3311e-128">-Confirm</span></span>
<span data-ttu-id="3311e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3311e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3311e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3311e-130">-WhatIf</span></span>
<span data-ttu-id="3311e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3311e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3311e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3311e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3311e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3311e-133">CommonParameters</span></span>
<span data-ttu-id="3311e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3311e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3311e-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3311e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3311e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3311e-136">INPUTS</span></span>

### <span data-ttu-id="3311e-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3311e-137">System.Guid</span></span>

### <span data-ttu-id="3311e-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="3311e-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="3311e-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3311e-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3311e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3311e-140">OUTPUTS</span></span>

### <span data-ttu-id="3311e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3311e-141">System.Boolean</span></span>

## <span data-ttu-id="3311e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="3311e-142">NOTES</span></span>

## <span data-ttu-id="3311e-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3311e-143">RELATED LINKS</span></span>
