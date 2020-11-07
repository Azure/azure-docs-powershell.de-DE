---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: f4c8a4fb3f10f7a019df95e82d7bbd3ad469411c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659563"
---
# <span data-ttu-id="04230-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="04230-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="04230-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04230-102">SYNOPSIS</span></span>
<span data-ttu-id="04230-103">Löscht eine Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="04230-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="04230-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04230-104">SYNTAX</span></span>

### <span data-ttu-id="04230-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="04230-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04230-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="04230-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04230-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04230-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04230-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04230-108">DESCRIPTION</span></span>
<span data-ttu-id="04230-109">Löscht eine Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="04230-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="04230-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04230-110">EXAMPLES</span></span>

### <span data-ttu-id="04230-111">Beispiel 1: Entfernen einer Gruppe nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="04230-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="04230-112">Entfernt die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" aus dem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="04230-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="04230-113">Beispiel 2 – Entfernen einer Gruppe nach Piping</span><span class="sxs-lookup"><span data-stu-id="04230-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="04230-114">Ruft die Gruppe mit der Objekt-ID "85F89C90-780E-4AA6-9F4F-6F268D322EEE" und Pipes ab, die Remove-AzADGroup, um die Gruppe aus dem Mandanten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="04230-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="04230-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="04230-115">PARAMETERS</span></span>

### <span data-ttu-id="04230-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04230-116">-DefaultProfile</span></span>
<span data-ttu-id="04230-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04230-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04230-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="04230-118">-DisplayName</span></span>
<span data-ttu-id="04230-119">Der Anzeigename der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="04230-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="04230-120">-Force</span><span class="sxs-lookup"><span data-stu-id="04230-120">-Force</span></span>
<span data-ttu-id="04230-121">Wenn angegeben, wird keine Bestätigung zum Löschen der Gruppe verlangt.</span><span class="sxs-lookup"><span data-stu-id="04230-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="04230-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="04230-122">-InputObject</span></span>
<span data-ttu-id="04230-123">Die Objektdarstellung der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="04230-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04230-124">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="04230-124">-ObjectId</span></span>
<span data-ttu-id="04230-125">Die Objekt-ID der zu entfernende Gruppe.</span><span class="sxs-lookup"><span data-stu-id="04230-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04230-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04230-126">-PassThru</span></span>
<span data-ttu-id="04230-127">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="04230-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="04230-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04230-128">-Confirm</span></span>
<span data-ttu-id="04230-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04230-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04230-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04230-130">-WhatIf</span></span>
<span data-ttu-id="04230-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04230-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04230-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04230-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04230-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04230-133">CommonParameters</span></span>
<span data-ttu-id="04230-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04230-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04230-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04230-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04230-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04230-136">INPUTS</span></span>

### <span data-ttu-id="04230-137">System. String</span><span class="sxs-lookup"><span data-stu-id="04230-137">System.String</span></span>

### <span data-ttu-id="04230-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="04230-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="04230-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04230-139">OUTPUTS</span></span>

### <span data-ttu-id="04230-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04230-140">System.Boolean</span></span>

## <span data-ttu-id="04230-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="04230-141">NOTES</span></span>

## <span data-ttu-id="04230-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04230-142">RELATED LINKS</span></span>
