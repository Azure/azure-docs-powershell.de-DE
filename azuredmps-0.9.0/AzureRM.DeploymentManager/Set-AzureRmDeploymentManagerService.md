---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474693"
---
# <span data-ttu-id="f3905-101">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="f3905-101">Set-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="f3905-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3905-102">SYNOPSIS</span></span>
<span data-ttu-id="f3905-103">Aktualisiert einen Dienst in der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="f3905-103">Updates a service in service topology.</span></span>

## <span data-ttu-id="f3905-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3905-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3905-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3905-105">DESCRIPTION</span></span>
<span data-ttu-id="f3905-106">Das Cmdlet " **Satz-AzureRmDeploymentManagerService** " aktualisiert einen Dienst mit dem angegebenen Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="f3905-106">The **Set-AzureRmDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="f3905-107">Das Cmdlet gibt das aktualisierte Dienstobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f3905-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="f3905-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3905-108">EXAMPLES</span></span>

### <span data-ttu-id="f3905-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3905-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="f3905-110">Mit diesem Befehl wird ein Dienst aktualisiert, dessen Name, Dienst topologiename und ResourceGroup den Eigenschaften Name, ServiceTopologyName und ResourceGroupName der $serviceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f3905-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="f3905-111">Der Dienst würde auf die Eigenschaften aktualisiert, die im $serviceObject gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="f3905-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="f3905-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3905-112">PARAMETERS</span></span>

### <span data-ttu-id="f3905-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3905-113">-DefaultProfile</span></span>
<span data-ttu-id="f3905-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3905-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3905-115">-Service</span><span class="sxs-lookup"><span data-stu-id="f3905-115">-Service</span></span>
<span data-ttu-id="f3905-116">Das Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="f3905-116">The service object.</span></span>

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

### <span data-ttu-id="f3905-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3905-117">-Confirm</span></span>
<span data-ttu-id="f3905-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3905-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3905-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3905-119">-WhatIf</span></span>
<span data-ttu-id="f3905-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3905-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3905-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3905-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3905-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3905-122">CommonParameters</span></span>
<span data-ttu-id="f3905-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3905-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3905-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3905-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3905-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3905-125">INPUTS</span></span>

### <span data-ttu-id="f3905-126">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="f3905-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="f3905-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3905-127">OUTPUTS</span></span>

### <span data-ttu-id="f3905-128">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="f3905-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="f3905-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3905-129">NOTES</span></span>

## <span data-ttu-id="f3905-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3905-130">RELATED LINKS</span></span>

[<span data-ttu-id="f3905-131">Neu – AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="f3905-131">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="f3905-132">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="f3905-132">Get-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="f3905-133">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="f3905-133">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)