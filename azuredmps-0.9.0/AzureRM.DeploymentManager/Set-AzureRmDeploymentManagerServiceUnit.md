---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475162"
---
# <span data-ttu-id="b3cf7-101">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3cf7-101">Set-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="b3cf7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cf7-103">Aktualisiert eine Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-103">Updates a service unit.</span></span>

## <span data-ttu-id="b3cf7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3cf7-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3cf7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3cf7-105">DESCRIPTION</span></span>
<span data-ttu-id="b3cf7-106">Das Cmdlet " **Satz-AzureRmDeploymentManagerServiceUnit** " aktualisiert eine Diensteinheit mit dem angegebenen Dienst Einheitenobjekt.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-106">The **Set-AzureRmDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="b3cf7-107">Das Cmdlet gibt das aktualisierte Dienst Einheitenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="b3cf7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3cf7-108">EXAMPLES</span></span>

### <span data-ttu-id="b3cf7-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3cf7-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="b3cf7-110">Mit diesem Befehl wird eine Diensteinheit aktualisiert, deren Name, Dienstname, Dienst topologiename und ResourceGroup mit den Eigenschaften Name, Service Name, ServiceTopologyName und ResourceGroupName der $serviceUnitObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="b3cf7-111">Der Befehl gibt das aktualisierte Dienst Einheitenobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="b3cf7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3cf7-112">PARAMETERS</span></span>

### <span data-ttu-id="b3cf7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3cf7-113">-DefaultProfile</span></span>
<span data-ttu-id="b3cf7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3cf7-115">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3cf7-115">-ServiceUnit</span></span>
<span data-ttu-id="b3cf7-116">Das Serviceeinheit-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-116">The service unit object.</span></span>

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

### <span data-ttu-id="b3cf7-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3cf7-117">-Confirm</span></span>
<span data-ttu-id="b3cf7-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3cf7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3cf7-119">-WhatIf</span></span>
<span data-ttu-id="b3cf7-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3cf7-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3cf7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cf7-122">CommonParameters</span></span>
<span data-ttu-id="b3cf7-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3cf7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cf7-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3cf7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cf7-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3cf7-125">INPUTS</span></span>

### <span data-ttu-id="b3cf7-126">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="b3cf7-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="b3cf7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3cf7-127">OUTPUTS</span></span>

### <span data-ttu-id="b3cf7-128">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="b3cf7-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="b3cf7-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3cf7-129">NOTES</span></span>

## <span data-ttu-id="b3cf7-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3cf7-130">RELATED LINKS</span></span>

[<span data-ttu-id="b3cf7-131">Neu – AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3cf7-131">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="b3cf7-132">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3cf7-132">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="b3cf7-133">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b3cf7-133">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)