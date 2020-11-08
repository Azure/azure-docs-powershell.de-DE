---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: a63bcfe0f807f36ffae5c10e644322b1fb612325
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176054"
---
# <span data-ttu-id="c53a5-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="c53a5-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="c53a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c53a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c53a5-103">Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="c53a5-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="c53a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c53a5-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c53a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c53a5-105">DESCRIPTION</span></span>
<span data-ttu-id="c53a5-106">Verwenden Sie **Update-AzServiceFabricReliability** , um die Zuverlässigkeit des primären Knotentyps in einem Cluster zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c53a5-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="c53a5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c53a5-107">EXAMPLES</span></span>

### <span data-ttu-id="c53a5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c53a5-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="c53a5-109">Mit diesem Befehl wird die Zuverlässigkeitsstufe des primären Knotentyps in Silver geändert.</span><span class="sxs-lookup"><span data-stu-id="c53a5-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="c53a5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c53a5-110">PARAMETERS</span></span>

### <span data-ttu-id="c53a5-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="c53a5-111">-AutoAddNode</span></span>
<span data-ttu-id="c53a5-112">Automatisches Hinzufügen von Knotenanzahl beim Ändern der Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="c53a5-112">Add node count automatically when changing reliability</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c53a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53a5-113">-DefaultProfile</span></span>
<span data-ttu-id="c53a5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c53a5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c53a5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c53a5-115">-Name</span></span>
<span data-ttu-id="c53a5-116">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="c53a5-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="c53a5-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="c53a5-117">-ReliabilityLevel</span></span>
<span data-ttu-id="c53a5-118">Zuverlässigkeitsstufe</span><span class="sxs-lookup"><span data-stu-id="c53a5-118">Reliability tier</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c53a5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c53a5-119">-ResourceGroupName</span></span>
<span data-ttu-id="c53a5-120">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c53a5-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c53a5-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c53a5-121">-Confirm</span></span>
<span data-ttu-id="c53a5-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c53a5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c53a5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c53a5-123">-WhatIf</span></span>
<span data-ttu-id="c53a5-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c53a5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c53a5-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c53a5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c53a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53a5-126">CommonParameters</span></span>
<span data-ttu-id="c53a5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c53a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53a5-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c53a5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53a5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c53a5-129">INPUTS</span></span>

### <span data-ttu-id="c53a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c53a5-130">System.String</span></span>

### <span data-ttu-id="c53a5-131">Microsoft. Azure. Commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="c53a5-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="c53a5-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="c53a5-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c53a5-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c53a5-133">OUTPUTS</span></span>

### <span data-ttu-id="c53a5-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c53a5-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c53a5-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c53a5-135">NOTES</span></span>

## <span data-ttu-id="c53a5-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c53a5-136">RELATED LINKS</span></span>
