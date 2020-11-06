---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: c8ee3324f7f6e7653d86bef747bdb9831982474e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481538"
---
# <span data-ttu-id="710ad-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="710ad-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="710ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="710ad-102">SYNOPSIS</span></span>
<span data-ttu-id="710ad-103">Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="710ad-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="710ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="710ad-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="710ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="710ad-105">DESCRIPTION</span></span>
<span data-ttu-id="710ad-106">Verwenden Sie **Update-AzureRmServiceFabricReliability** , um die Zuverlässigkeit des primären Knotentyps in einem Cluster zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="710ad-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="710ad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="710ad-107">EXAMPLES</span></span>

### <span data-ttu-id="710ad-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="710ad-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="710ad-109">Mit diesem Befehl wird die Zuverlässigkeitsstufe des primären Knotentyps in Silver geändert.</span><span class="sxs-lookup"><span data-stu-id="710ad-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="710ad-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="710ad-110">PARAMETERS</span></span>

### <span data-ttu-id="710ad-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="710ad-111">-AutoAddNode</span></span>
<span data-ttu-id="710ad-112">Automatisches Hinzufügen der Knotenanzahl beim Ändern der Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="710ad-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="710ad-113">-Name</span><span class="sxs-lookup"><span data-stu-id="710ad-113">-Name</span></span>
<span data-ttu-id="710ad-114">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="710ad-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="710ad-115">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="710ad-115">-ReliabilityLevel</span></span>
<span data-ttu-id="710ad-116">Zuverlässigkeitsstufe</span><span class="sxs-lookup"><span data-stu-id="710ad-116">Reliability tier.</span></span>

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

### <span data-ttu-id="710ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="710ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="710ad-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="710ad-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="710ad-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="710ad-119">-Confirm</span></span>
<span data-ttu-id="710ad-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="710ad-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="710ad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="710ad-121">-WhatIf</span></span>
<span data-ttu-id="710ad-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="710ad-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="710ad-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="710ad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="710ad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="710ad-124">-DefaultProfile</span></span>
<span data-ttu-id="710ad-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="710ad-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="710ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="710ad-126">CommonParameters</span></span>
<span data-ttu-id="710ad-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="710ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="710ad-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="710ad-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="710ad-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="710ad-129">INPUTS</span></span>

### <span data-ttu-id="710ad-130">Microsoft. Azure. Commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="710ad-130">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="710ad-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="710ad-131">System.Management.Automation.SwitchParameter</span></span>

<span data-ttu-id="710ad-132">System. String</span><span class="sxs-lookup"><span data-stu-id="710ad-132">System.String</span></span>

## <span data-ttu-id="710ad-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="710ad-133">OUTPUTS</span></span>

### <span data-ttu-id="710ad-134">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="710ad-134">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="710ad-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="710ad-135">NOTES</span></span>

## <span data-ttu-id="710ad-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="710ad-136">RELATED LINKS</span></span>

