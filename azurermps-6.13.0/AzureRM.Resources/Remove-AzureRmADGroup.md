---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
ms.openlocfilehash: f9aa1f3d45a50a59c118abea4278bfed1725fa9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482110"
---
# <span data-ttu-id="f5dea-101">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="f5dea-101">Remove-AzureRmADGroup</span></span>

## <span data-ttu-id="f5dea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5dea-102">SYNOPSIS</span></span>
<span data-ttu-id="f5dea-103">Löscht eine Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f5dea-103">Deletes an active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5dea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5dea-104">SYNTAX</span></span>

### <span data-ttu-id="f5dea-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f5dea-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dea-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5dea-106">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dea-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5dea-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5dea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5dea-108">DESCRIPTION</span></span>
<span data-ttu-id="f5dea-109">Löscht eine Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f5dea-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="f5dea-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5dea-110">EXAMPLES</span></span>

### <span data-ttu-id="f5dea-111">Beispiel 1: Entfernen einer Gruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="f5dea-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="f5dea-112">Entfernt die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="f5dea-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="f5dea-113">Beispiel 2 – Entfernen einer Gruppe nach Piping</span><span class="sxs-lookup"><span data-stu-id="f5dea-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroup
```

<span data-ttu-id="f5dea-114">Ruft die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" und Pipes ab, die Remove-AzureRmADGroup, um die Gruppe aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f5dea-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzureRmADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="f5dea-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5dea-115">PARAMETERS</span></span>

### <span data-ttu-id="f5dea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5dea-116">-DefaultProfile</span></span>
<span data-ttu-id="f5dea-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5dea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5dea-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f5dea-118">-DisplayName</span></span>
<span data-ttu-id="f5dea-119">Der Anzeigename der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f5dea-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="f5dea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f5dea-120">-Force</span></span>
<span data-ttu-id="f5dea-121">Wenn angegeben, wird keine Bestätigung zum Löschen der Gruppe verlangt.</span><span class="sxs-lookup"><span data-stu-id="f5dea-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="f5dea-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5dea-122">-InputObject</span></span>
<span data-ttu-id="f5dea-123">Die Objektdarstellung der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f5dea-123">The object representation of the group to be removed.</span></span>

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

### <span data-ttu-id="f5dea-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="f5dea-124">-ObjectId</span></span>
<span data-ttu-id="f5dea-125">Die Objekt-ID der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f5dea-125">The object id of the group to be removed.</span></span>

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

### <span data-ttu-id="f5dea-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5dea-126">-PassThru</span></span>
<span data-ttu-id="f5dea-127">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f5dea-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f5dea-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5dea-128">-Confirm</span></span>
<span data-ttu-id="f5dea-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5dea-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5dea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5dea-130">-WhatIf</span></span>
<span data-ttu-id="f5dea-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5dea-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5dea-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5dea-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5dea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5dea-133">CommonParameters</span></span>
<span data-ttu-id="f5dea-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5dea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5dea-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5dea-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5dea-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5dea-136">INPUTS</span></span>

### <span data-ttu-id="f5dea-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f5dea-137">System.Guid</span></span>

### <span data-ttu-id="f5dea-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="f5dea-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="f5dea-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f5dea-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f5dea-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5dea-140">OUTPUTS</span></span>

### <span data-ttu-id="f5dea-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5dea-141">System.Boolean</span></span>

## <span data-ttu-id="f5dea-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5dea-142">NOTES</span></span>

## <span data-ttu-id="f5dea-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5dea-143">RELATED LINKS</span></span>
