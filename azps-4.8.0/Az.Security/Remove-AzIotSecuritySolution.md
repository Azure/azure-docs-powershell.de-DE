---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174181"
---
# <span data-ttu-id="78fd1-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="78fd1-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="78fd1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="78fd1-103">Viel Sicherheitslösung löschen</span><span class="sxs-lookup"><span data-stu-id="78fd1-103">Delete IoT security solution</span></span>

## <span data-ttu-id="78fd1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78fd1-104">SYNTAX</span></span>

### <span data-ttu-id="78fd1-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="78fd1-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78fd1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="78fd1-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78fd1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="78fd1-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78fd1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78fd1-108">DESCRIPTION</span></span>
<span data-ttu-id="78fd1-109">Das Remove-AzIotSecuritySolution-Cmdlet löscht eine bestimmte viel Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="78fd1-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="78fd1-110">Die Sicherheitslösung "viel" sammelt Sicherheitsdaten und Ereignisse von viel-Geräten und viel Hub, um Bedrohungen zu verhindern und zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="78fd1-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="78fd1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78fd1-111">EXAMPLES</span></span>

### <span data-ttu-id="78fd1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78fd1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="78fd1-113">Löschen der Sicherheitslösung "MySample" mit der Ressourcengruppe "myresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="78fd1-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="78fd1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="78fd1-114">PARAMETERS</span></span>

### <span data-ttu-id="78fd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fd1-115">-DefaultProfile</span></span>
<span data-ttu-id="78fd1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78fd1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78fd1-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="78fd1-117">-InputObject</span></span>
<span data-ttu-id="78fd1-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="78fd1-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78fd1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="78fd1-119">-Name</span></span>
<span data-ttu-id="78fd1-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="78fd1-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78fd1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78fd1-121">-PassThru</span></span>
<span data-ttu-id="78fd1-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="78fd1-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="78fd1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78fd1-123">-ResourceGroupName</span></span>
<span data-ttu-id="78fd1-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78fd1-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78fd1-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="78fd1-125">-ResourceId</span></span>
<span data-ttu-id="78fd1-126">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="78fd1-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78fd1-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78fd1-127">-Confirm</span></span>
<span data-ttu-id="78fd1-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78fd1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78fd1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78fd1-129">-WhatIf</span></span>
<span data-ttu-id="78fd1-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78fd1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78fd1-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78fd1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78fd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fd1-132">CommonParameters</span></span>
<span data-ttu-id="78fd1-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78fd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fd1-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78fd1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fd1-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78fd1-135">INPUTS</span></span>

### <span data-ttu-id="78fd1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="78fd1-136">System.String</span></span>

### <span data-ttu-id="78fd1-137">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="78fd1-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="78fd1-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78fd1-138">OUTPUTS</span></span>

### <span data-ttu-id="78fd1-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78fd1-139">System.Boolean</span></span>

## <span data-ttu-id="78fd1-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="78fd1-140">NOTES</span></span>

## <span data-ttu-id="78fd1-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78fd1-141">RELATED LINKS</span></span>
