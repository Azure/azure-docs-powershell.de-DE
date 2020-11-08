---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179659"
---
# <span data-ttu-id="b258c-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="b258c-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="b258c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b258c-102">SYNOPSIS</span></span>
<span data-ttu-id="b258c-103">Ändern des Service Fabric-Upgrade-Typs des Clusters</span><span class="sxs-lookup"><span data-stu-id="b258c-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="b258c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b258c-104">SYNTAX</span></span>

### <span data-ttu-id="b258c-105">Automatisch</span><span class="sxs-lookup"><span data-stu-id="b258c-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b258c-106">Manuell</span><span class="sxs-lookup"><span data-stu-id="b258c-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b258c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b258c-107">DESCRIPTION</span></span>
<span data-ttu-id="b258c-108">Verwenden Sie " **AzServiceFabricUpgradeType** ", um den Upgradetyp auf "automatisch" oder "manuell" mit spezieller Service Fabric-Code Version zu setzen.</span><span class="sxs-lookup"><span data-stu-id="b258c-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="b258c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b258c-109">EXAMPLES</span></span>

### <span data-ttu-id="b258c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b258c-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="b258c-111">Mit diesem Befehl wird der Cluster Aktualisierungsmodus auf Automatic gesetzt.</span><span class="sxs-lookup"><span data-stu-id="b258c-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="b258c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b258c-112">PARAMETERS</span></span>

### <span data-ttu-id="b258c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b258c-113">-DefaultProfile</span></span>
<span data-ttu-id="b258c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b258c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b258c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b258c-115">-Name</span></span>
<span data-ttu-id="b258c-116">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="b258c-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b258c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b258c-117">-ResourceGroupName</span></span>
<span data-ttu-id="b258c-118">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b258c-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b258c-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="b258c-119">-UpgradeMode</span></span>
<span data-ttu-id="b258c-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="b258c-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b258c-121">-Version</span><span class="sxs-lookup"><span data-stu-id="b258c-121">-Version</span></span>
<span data-ttu-id="b258c-122">Cluster Code Version</span><span class="sxs-lookup"><span data-stu-id="b258c-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b258c-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b258c-123">-Confirm</span></span>
<span data-ttu-id="b258c-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b258c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b258c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b258c-125">-WhatIf</span></span>
<span data-ttu-id="b258c-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b258c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b258c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b258c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b258c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b258c-128">CommonParameters</span></span>
<span data-ttu-id="b258c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b258c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b258c-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b258c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b258c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b258c-131">INPUTS</span></span>

### <span data-ttu-id="b258c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b258c-132">System.String</span></span>

### <span data-ttu-id="b258c-133">Microsoft. Azure. Commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="b258c-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="b258c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b258c-134">OUTPUTS</span></span>

### <span data-ttu-id="b258c-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b258c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b258c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b258c-136">NOTES</span></span>

## <span data-ttu-id="b258c-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b258c-137">RELATED LINKS</span></span>
