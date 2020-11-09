---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297124"
---
# <span data-ttu-id="6b1f5-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="6b1f5-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="6b1f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1f5-103">Aktualisiert die Serviceeinheit.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-103">Updates the service unit.</span></span>

## <span data-ttu-id="6b1f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b1f5-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b1f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b1f5-105">DESCRIPTION</span></span>
<span data-ttu-id="6b1f5-106">Das Cmdlet " **Satz-AzDeploymentManagerServiceUnit** " aktualisiert eine Diensteinheit mit dem angegebenen Dienst Einheitenobjekt.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="6b1f5-107">Das Cmdlet gibt das aktualisierte Dienst Einheitenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="6b1f5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b1f5-108">EXAMPLES</span></span>

### <span data-ttu-id="6b1f5-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b1f5-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="6b1f5-110">Mit diesem Befehl wird eine Diensteinheit aktualisiert, deren Name, Dienstname, Dienst topologiename und ResourceGroup mit den Eigenschaften Name, Service Name, ServiceTopologyName und ResourceGroupName der $serviceUnitObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="6b1f5-111">Der Befehl gibt das aktualisierte Dienst Einheitenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="6b1f5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b1f5-112">PARAMETERS</span></span>

### <span data-ttu-id="6b1f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1f5-113">-DefaultProfile</span></span>
<span data-ttu-id="6b1f5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b1f5-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6b1f5-115">-InputObject</span></span>
<span data-ttu-id="6b1f5-116">Das Serviceeinheit-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1f5-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b1f5-117">-Confirm</span></span>
<span data-ttu-id="6b1f5-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b1f5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b1f5-119">-WhatIf</span></span>
<span data-ttu-id="6b1f5-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b1f5-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b1f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1f5-122">CommonParameters</span></span>
<span data-ttu-id="6b1f5-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1f5-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b1f5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1f5-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b1f5-125">INPUTS</span></span>

### <span data-ttu-id="6b1f5-126">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="6b1f5-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="6b1f5-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b1f5-127">OUTPUTS</span></span>

### <span data-ttu-id="6b1f5-128">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="6b1f5-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="6b1f5-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b1f5-129">NOTES</span></span>

## <span data-ttu-id="6b1f5-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b1f5-130">RELATED LINKS</span></span>
