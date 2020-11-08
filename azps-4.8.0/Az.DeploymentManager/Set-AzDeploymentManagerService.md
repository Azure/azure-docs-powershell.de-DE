---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173012"
---
# <span data-ttu-id="0d85e-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="0d85e-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="0d85e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d85e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d85e-103">Aktualisiert den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0d85e-103">Updates the service.</span></span>

## <span data-ttu-id="0d85e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d85e-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d85e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d85e-105">DESCRIPTION</span></span>
<span data-ttu-id="0d85e-106">Das Cmdlet " **Satz-AzDeploymentManagerService** " aktualisiert einen Dienst mit dem angegebenen Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="0d85e-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="0d85e-107">Das Cmdlet gibt das aktualisierte Dienstobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0d85e-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="0d85e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d85e-108">EXAMPLES</span></span>

### <span data-ttu-id="0d85e-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d85e-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="0d85e-110">Mit diesem Befehl wird ein Dienst aktualisiert, dessen Name, Dienst topologiename und ResourceGroup den Eigenschaften Name, ServiceTopologyName und ResourceGroupName der $serviceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0d85e-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="0d85e-111">Der Dienst würde auf die Eigenschaften aktualisiert, die im $serviceObject gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="0d85e-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="0d85e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d85e-112">PARAMETERS</span></span>

### <span data-ttu-id="0d85e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d85e-113">-DefaultProfile</span></span>
<span data-ttu-id="0d85e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d85e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d85e-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d85e-115">-InputObject</span></span>
<span data-ttu-id="0d85e-116">Das Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="0d85e-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d85e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d85e-117">-Confirm</span></span>
<span data-ttu-id="0d85e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d85e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d85e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d85e-119">-WhatIf</span></span>
<span data-ttu-id="0d85e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d85e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d85e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d85e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d85e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d85e-122">CommonParameters</span></span>
<span data-ttu-id="0d85e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d85e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d85e-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d85e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d85e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d85e-125">INPUTS</span></span>

### <span data-ttu-id="0d85e-126">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="0d85e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="0d85e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d85e-127">OUTPUTS</span></span>

### <span data-ttu-id="0d85e-128">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="0d85e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="0d85e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d85e-129">NOTES</span></span>

## <span data-ttu-id="0d85e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d85e-130">RELATED LINKS</span></span>
