---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7b04fc95af1ee340e87fa5ed46cbba9f1956d9e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474737"
---
# <span data-ttu-id="da4f9-101">New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="da4f9-101">New-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="da4f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="da4f9-103">Erstellt einen neuen Bereitstellungsschritt.</span><span class="sxs-lookup"><span data-stu-id="da4f9-103">Creates a new deployment step.</span></span>

## <span data-ttu-id="da4f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da4f9-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -Duration <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da4f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da4f9-105">DESCRIPTION</span></span>
<span data-ttu-id="da4f9-106">Das Cmdlet **New-AzureRmDeploymentManagerStep** erstellt einen Bereitstellungsschritt, auf den in Rollouts verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="da4f9-106">The **New-AzureRmDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="da4f9-107">Geben Sie den *Namen* , die *ResourceGroupName* und die erforderlichen Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="da4f9-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="da4f9-108">Sie können das zurückgegebene Objekt lokal ändern und dann die Änderungen auf den Schritt mithilfe des Set-AzureRmDeploymentManagerStep-Cmdlets anwenden.</span><span class="sxs-lookup"><span data-stu-id="da4f9-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="da4f9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da4f9-109">EXAMPLES</span></span>

### <span data-ttu-id="da4f9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da4f9-110">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="da4f9-111">Erstellt einen Schritt im ContosoResourceGroup mit dem Namen ContosoService1WaitStep mit dem zentralen US-Standort als Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="da4f9-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="da4f9-112">Die Duration-Eigenschaft gibt die Dauer an, die das Rollout wartet, bevor der nächste Schritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da4f9-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="da4f9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="da4f9-113">PARAMETERS</span></span>

### <span data-ttu-id="da4f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da4f9-114">-DefaultProfile</span></span>
<span data-ttu-id="da4f9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da4f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da4f9-116">-Dauer</span><span class="sxs-lookup"><span data-stu-id="da4f9-116">-Duration</span></span>
<span data-ttu-id="da4f9-117">Die Dauer, die im ISO 8601-Format gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da4f9-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="da4f9-118">Z. b.: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="da4f9-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="da4f9-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="da4f9-119">-Location</span></span>
<span data-ttu-id="da4f9-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="da4f9-120">The location of the resource.</span></span>

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

### <span data-ttu-id="da4f9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="da4f9-121">-Name</span></span>
<span data-ttu-id="da4f9-122">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="da4f9-122">The name of the step.</span></span>

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

### <span data-ttu-id="da4f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da4f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="da4f9-124">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da4f9-124">The resource group.</span></span>

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

### <span data-ttu-id="da4f9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="da4f9-125">-Tag</span></span>
<span data-ttu-id="da4f9-126">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="da4f9-126">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da4f9-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da4f9-127">-Confirm</span></span>
<span data-ttu-id="da4f9-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da4f9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da4f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da4f9-129">-WhatIf</span></span>
<span data-ttu-id="da4f9-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da4f9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da4f9-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da4f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da4f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4f9-132">CommonParameters</span></span>
<span data-ttu-id="da4f9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da4f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="da4f9-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da4f9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4f9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da4f9-135">INPUTS</span></span>

### <span data-ttu-id="da4f9-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="da4f9-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="da4f9-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da4f9-137">OUTPUTS</span></span>

### <span data-ttu-id="da4f9-138">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="da4f9-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="da4f9-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="da4f9-139">NOTES</span></span>

## <span data-ttu-id="da4f9-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da4f9-140">RELATED LINKS</span></span>
