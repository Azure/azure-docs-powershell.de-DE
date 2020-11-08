---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179784"
---
# <span data-ttu-id="2e96c-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="2e96c-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="2e96c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e96c-102">SYNOPSIS</span></span>
<span data-ttu-id="2e96c-103">Konfiguriert ein neues Stack-Edge-Gerät</span><span class="sxs-lookup"><span data-stu-id="2e96c-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="2e96c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e96c-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e96c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e96c-105">DESCRIPTION</span></span>
<span data-ttu-id="2e96c-106">Das Cmdlet " **New-AzStackEdgeDevice** " konfiguriert ein neues Stack-Edge-Gerät</span><span class="sxs-lookup"><span data-stu-id="2e96c-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="2e96c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e96c-107">EXAMPLES</span></span>

### <span data-ttu-id="2e96c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2e96c-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="2e96c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e96c-109">PARAMETERS</span></span>

### <span data-ttu-id="2e96c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e96c-110">-AsJob</span></span>
<span data-ttu-id="2e96c-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2e96c-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e96c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e96c-112">-DefaultProfile</span></span>
<span data-ttu-id="2e96c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e96c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e96c-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="2e96c-114">-Location</span></span>
<span data-ttu-id="2e96c-115">Standort des Geräts</span><span class="sxs-lookup"><span data-stu-id="2e96c-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e96c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2e96c-116">-Name</span></span>
<span data-ttu-id="2e96c-117">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="2e96c-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e96c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e96c-118">-ResourceGroupName</span></span>
<span data-ttu-id="2e96c-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2e96c-119">Resource Group Name</span></span>

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

### <span data-ttu-id="2e96c-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="2e96c-120">-Sku</span></span>
<span data-ttu-id="2e96c-121">Verfügbare SKUs sind Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="2e96c-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e96c-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e96c-122">-Confirm</span></span>
<span data-ttu-id="2e96c-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e96c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e96c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e96c-124">-WhatIf</span></span>
<span data-ttu-id="2e96c-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e96c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e96c-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e96c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e96c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e96c-127">CommonParameters</span></span>
<span data-ttu-id="2e96c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e96c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e96c-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e96c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e96c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e96c-130">INPUTS</span></span>

### <span data-ttu-id="2e96c-131">Keine</span><span class="sxs-lookup"><span data-stu-id="2e96c-131">None</span></span>

## <span data-ttu-id="2e96c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e96c-132">OUTPUTS</span></span>

### <span data-ttu-id="2e96c-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="2e96c-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="2e96c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e96c-134">NOTES</span></span>

## <span data-ttu-id="2e96c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e96c-135">RELATED LINKS</span></span>
