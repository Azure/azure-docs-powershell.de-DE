---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 7884e45c2b4f635c9236f213a93eb69524b37fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662611"
---
# <span data-ttu-id="cd271-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="cd271-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="cd271-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd271-102">SYNOPSIS</span></span>
<span data-ttu-id="cd271-103">Ändern des Service Fabric-Upgrade-Typs des Clusters</span><span class="sxs-lookup"><span data-stu-id="cd271-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd271-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd271-104">SYNTAX</span></span>

### <span data-ttu-id="cd271-105">Automatisch</span><span class="sxs-lookup"><span data-stu-id="cd271-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd271-106">Manuell</span><span class="sxs-lookup"><span data-stu-id="cd271-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd271-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd271-107">DESCRIPTION</span></span>
<span data-ttu-id="cd271-108">Verwenden Sie " **AzureRmServiceFabricUpgradeType** ", um den Upgradetyp auf "automatisch" oder "manuell" mit spezieller Service Fabric-Code Version zu setzen.</span><span class="sxs-lookup"><span data-stu-id="cd271-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="cd271-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd271-109">EXAMPLES</span></span>

### <span data-ttu-id="cd271-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cd271-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="cd271-111">Mit diesem Befehl wird der Cluster Aktualisierungsmodus auf Automatic gesetzt.</span><span class="sxs-lookup"><span data-stu-id="cd271-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="cd271-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd271-112">PARAMETERS</span></span>

### <span data-ttu-id="cd271-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cd271-113">-Name</span></span>
<span data-ttu-id="cd271-114">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="cd271-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cd271-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd271-115">-ResourceGroupName</span></span>
<span data-ttu-id="cd271-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cd271-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cd271-117">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cd271-117">-UpgradeMode</span></span>
<span data-ttu-id="cd271-118">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cd271-118">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="cd271-119">-Version</span><span class="sxs-lookup"><span data-stu-id="cd271-119">-Version</span></span>
<span data-ttu-id="cd271-120">Cluster Code Version.</span><span class="sxs-lookup"><span data-stu-id="cd271-120">Cluster code version.</span></span>

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

### <span data-ttu-id="cd271-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd271-121">-Confirm</span></span>
<span data-ttu-id="cd271-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd271-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd271-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd271-123">-WhatIf</span></span>
<span data-ttu-id="cd271-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd271-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd271-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd271-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd271-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd271-126">-DefaultProfile</span></span>
<span data-ttu-id="cd271-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd271-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd271-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd271-128">CommonParameters</span></span>
<span data-ttu-id="cd271-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd271-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd271-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd271-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd271-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd271-131">INPUTS</span></span>

### <span data-ttu-id="cd271-132">Microsoft. Azure. Commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cd271-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="cd271-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cd271-133">System.String</span></span>

## <span data-ttu-id="cd271-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd271-134">OUTPUTS</span></span>

### <span data-ttu-id="cd271-135">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="cd271-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="cd271-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd271-136">NOTES</span></span>

## <span data-ttu-id="cd271-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd271-137">RELATED LINKS</span></span>

