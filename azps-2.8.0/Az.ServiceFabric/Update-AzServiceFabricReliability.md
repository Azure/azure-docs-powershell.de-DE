---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: 343c5c1a35334a25643aea576a9c545d1349e1f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824675"
---
# <span data-ttu-id="f02d7-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f02d7-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="f02d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f02d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f02d7-103">Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="f02d7-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="f02d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f02d7-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f02d7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f02d7-105">DESCRIPTION</span></span>
<span data-ttu-id="f02d7-106">Verwenden Sie **Update-AzServiceFabricReliability** , um die Zuverlässigkeit des primären Knotentyps in einem Cluster zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f02d7-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="f02d7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f02d7-107">EXAMPLES</span></span>

### <span data-ttu-id="f02d7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f02d7-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="f02d7-109">Mit diesem Befehl wird die Zuverlässigkeitsstufe des primären Knotentyps in Silver geändert.</span><span class="sxs-lookup"><span data-stu-id="f02d7-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="f02d7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f02d7-110">PARAMETERS</span></span>

### <span data-ttu-id="f02d7-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="f02d7-111">-AutoAddNode</span></span>
<span data-ttu-id="f02d7-112">Automatisches Hinzufügen von Knotenanzahl beim Ändern der Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="f02d7-112">Add node count automatically when changing reliability</span></span>

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

### <span data-ttu-id="f02d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02d7-113">-DefaultProfile</span></span>
<span data-ttu-id="f02d7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f02d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f02d7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f02d7-115">-Name</span></span>
<span data-ttu-id="f02d7-116">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="f02d7-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="f02d7-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="f02d7-117">-ReliabilityLevel</span></span>
<span data-ttu-id="f02d7-118">Zuverlässigkeitsstufe</span><span class="sxs-lookup"><span data-stu-id="f02d7-118">Reliability tier</span></span>

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

### <span data-ttu-id="f02d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f02d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="f02d7-120">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f02d7-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f02d7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f02d7-121">-Confirm</span></span>
<span data-ttu-id="f02d7-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f02d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f02d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f02d7-123">-WhatIf</span></span>
<span data-ttu-id="f02d7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f02d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f02d7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f02d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f02d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02d7-126">CommonParameters</span></span>
<span data-ttu-id="f02d7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02d7-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f02d7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02d7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f02d7-129">INPUTS</span></span>

### <span data-ttu-id="f02d7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f02d7-130">System.String</span></span>

### <span data-ttu-id="f02d7-131">Microsoft. Azure. Commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="f02d7-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="f02d7-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f02d7-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f02d7-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f02d7-133">OUTPUTS</span></span>

### <span data-ttu-id="f02d7-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="f02d7-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f02d7-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f02d7-135">NOTES</span></span>

## <span data-ttu-id="f02d7-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f02d7-136">RELATED LINKS</span></span>
