---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7241e072109583b7afc24fc3f69746599bd67c53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475161"
---
# <span data-ttu-id="da5d1-101">Set-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="da5d1-101">Set-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="da5d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="da5d1-103">Aktualisiert einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="da5d1-103">Updates a step.</span></span>

## <span data-ttu-id="da5d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da5d1-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da5d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da5d1-105">DESCRIPTION</span></span>
<span data-ttu-id="da5d1-106">Das Cmdlet " **Satz-AzureRmDeploymentManagerStep** " aktualisiert einen Schritt mit dem angegebenen Step-Objekt.</span><span class="sxs-lookup"><span data-stu-id="da5d1-106">The **Set-AzureRmDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="da5d1-107">Das Cmdlet gibt das aktualisierte Step-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="da5d1-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="da5d1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da5d1-108">EXAMPLES</span></span>

### <span data-ttu-id="da5d1-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da5d1-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerStep -Step $stepObject
```

<span data-ttu-id="da5d1-110">Mit diesem Befehl wird ein Schritt aktualisiert, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $stepObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="da5d1-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="da5d1-111">Der Schritt würde auf die Eigenschaften aktualisiert, die im $stepObject gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="da5d1-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="da5d1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="da5d1-112">PARAMETERS</span></span>

### <span data-ttu-id="da5d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5d1-113">-DefaultProfile</span></span>
<span data-ttu-id="da5d1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da5d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da5d1-115">-Step</span><span class="sxs-lookup"><span data-stu-id="da5d1-115">-Step</span></span>
<span data-ttu-id="da5d1-116">Das Step-Objekt.</span><span class="sxs-lookup"><span data-stu-id="da5d1-116">The step object.</span></span>

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

### <span data-ttu-id="da5d1-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da5d1-117">-Confirm</span></span>
<span data-ttu-id="da5d1-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da5d1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da5d1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da5d1-119">-WhatIf</span></span>
<span data-ttu-id="da5d1-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da5d1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da5d1-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da5d1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da5d1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5d1-122">CommonParameters</span></span>
<span data-ttu-id="da5d1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da5d1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="da5d1-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da5d1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5d1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da5d1-125">INPUTS</span></span>

### <span data-ttu-id="da5d1-126">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="da5d1-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="da5d1-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da5d1-127">OUTPUTS</span></span>

### <span data-ttu-id="da5d1-128">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="da5d1-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="da5d1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="da5d1-129">NOTES</span></span>

## <span data-ttu-id="da5d1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da5d1-130">RELATED LINKS</span></span>
