---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661197"
---
# <span data-ttu-id="a99f6-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="a99f6-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="a99f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a99f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a99f6-103">Erstellt einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="a99f6-103">Creates a step.</span></span>

## <span data-ttu-id="a99f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a99f6-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a99f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a99f6-105">DESCRIPTION</span></span>
<span data-ttu-id="a99f6-106">Das Cmdlet **New-AzDeploymentManagerStep** erstellt einen Bereitstellungsschritt, auf den in Rollouts verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a99f6-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="a99f6-107">Geben Sie den *Namen* , die *ResourceGroupName* und die erforderlichen Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="a99f6-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="a99f6-108">Sie können das zurückgegebene Objekt lokal ändern und dann die Änderungen auf den Schritt mithilfe des Set-AzDeploymentManagerStep-Cmdlets anwenden.</span><span class="sxs-lookup"><span data-stu-id="a99f6-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="a99f6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a99f6-109">EXAMPLES</span></span>

### <span data-ttu-id="a99f6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a99f6-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="a99f6-111">Erstellt einen Schritt im ContosoResourceGroup mit dem Namen ContosoService1WaitStep mit dem zentralen US-Standort als Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a99f6-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="a99f6-112">Die Duration-Eigenschaft gibt die Dauer an, die das Rollout wartet, bevor der nächste Schritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a99f6-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="a99f6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a99f6-113">PARAMETERS</span></span>

### <span data-ttu-id="a99f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99f6-114">-DefaultProfile</span></span>
<span data-ttu-id="a99f6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a99f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a99f6-116">-Dauer</span><span class="sxs-lookup"><span data-stu-id="a99f6-116">-Duration</span></span>
<span data-ttu-id="a99f6-117">Die Dauer, die im ISO 8601-Format gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a99f6-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="a99f6-118">Z. b.: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="a99f6-118">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99f6-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="a99f6-119">-Location</span></span>
<span data-ttu-id="a99f6-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a99f6-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99f6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a99f6-121">-Name</span></span>
<span data-ttu-id="a99f6-122">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="a99f6-122">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a99f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="a99f6-124">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a99f6-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99f6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a99f6-125">-Tag</span></span>
<span data-ttu-id="a99f6-126">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="a99f6-126">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a99f6-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a99f6-127">-Confirm</span></span>
<span data-ttu-id="a99f6-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a99f6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a99f6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a99f6-129">-WhatIf</span></span>
<span data-ttu-id="a99f6-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a99f6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a99f6-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a99f6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a99f6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99f6-132">CommonParameters</span></span>
<span data-ttu-id="a99f6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99f6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99f6-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99f6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99f6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a99f6-135">INPUTS</span></span>

### <span data-ttu-id="a99f6-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a99f6-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a99f6-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a99f6-137">OUTPUTS</span></span>

### <span data-ttu-id="a99f6-138">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="a99f6-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="a99f6-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a99f6-139">NOTES</span></span>

## <span data-ttu-id="a99f6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a99f6-140">RELATED LINKS</span></span>
