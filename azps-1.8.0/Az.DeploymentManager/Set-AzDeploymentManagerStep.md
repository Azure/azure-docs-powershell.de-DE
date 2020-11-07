---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 15944b324cc2b33d3186d7c84da16c72351dcc99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661173"
---
# <span data-ttu-id="ff526-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="ff526-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="ff526-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff526-102">SYNOPSIS</span></span>
<span data-ttu-id="ff526-103">Aktualisiert den Schritt.</span><span class="sxs-lookup"><span data-stu-id="ff526-103">Updates the step.</span></span>

## <span data-ttu-id="ff526-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff526-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff526-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff526-105">DESCRIPTION</span></span>
<span data-ttu-id="ff526-106">Das Cmdlet " **Satz-AzDeploymentManagerStep** " aktualisiert einen Schritt mit dem angegebenen Step-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff526-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="ff526-107">Das Cmdlet gibt das aktualisierte Step-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ff526-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="ff526-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff526-108">EXAMPLES</span></span>

### <span data-ttu-id="ff526-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff526-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="ff526-110">Mit diesem Befehl wird ein Schritt aktualisiert, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $stepObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ff526-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="ff526-111">Der Schritt würde auf die Eigenschaften aktualisiert, die im $stepObject gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="ff526-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="ff526-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff526-112">PARAMETERS</span></span>

### <span data-ttu-id="ff526-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff526-113">-DefaultProfile</span></span>
<span data-ttu-id="ff526-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff526-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff526-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ff526-115">-InputObject</span></span>
<span data-ttu-id="ff526-116">Das Step-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff526-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff526-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ff526-117">-Confirm</span></span>
<span data-ttu-id="ff526-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff526-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff526-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff526-119">-WhatIf</span></span>
<span data-ttu-id="ff526-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff526-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff526-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff526-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff526-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff526-122">CommonParameters</span></span>
<span data-ttu-id="ff526-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff526-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff526-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff526-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff526-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff526-125">INPUTS</span></span>

### <span data-ttu-id="ff526-126">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ff526-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ff526-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff526-127">OUTPUTS</span></span>

### <span data-ttu-id="ff526-128">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ff526-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ff526-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff526-129">NOTES</span></span>

## <span data-ttu-id="ff526-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff526-130">RELATED LINKS</span></span>
