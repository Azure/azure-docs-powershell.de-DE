---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172254"
---
# <span data-ttu-id="c67e1-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="c67e1-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="c67e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c67e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c67e1-103">Löst eine Auswertung der Richtlinienkonformität für alle Ressourcen in einem Abonnement oder einer Ressourcengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="c67e1-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="c67e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c67e1-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c67e1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c67e1-105">DESCRIPTION</span></span>
<span data-ttu-id="c67e1-106">Das **Cmdlet "Start-AzPolicyComplianceScan"** startet eine Richtliniencomplianceauswertung für ein Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c67e1-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="c67e1-107">Für alle Ressourcen innerhalb dieses Bereichs wird der Compliancestatus anhand aller zugewiesenen Richtlinien ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="c67e1-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="c67e1-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c67e1-108">EXAMPLES</span></span>

### <span data-ttu-id="c67e1-109">Beispiel 1: Starten einer Compliancescan im Abonnementbereich</span><span class="sxs-lookup"><span data-stu-id="c67e1-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="c67e1-110">Mit diesem Befehl wird eine Richtlinienkonformitätsauswertung für das aktive Abonnement gestartet.</span><span class="sxs-lookup"><span data-stu-id="c67e1-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="c67e1-111">Beispiel 2: Starten einer Compliancescan im Bereich "Ressourcengruppe"</span><span class="sxs-lookup"><span data-stu-id="c67e1-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="c67e1-112">Mit diesem Befehl wird eine Richtlinienkonformitätsauswertung für die Ressourcengruppe "myRG" im aktiven Abonnement gestartet.</span><span class="sxs-lookup"><span data-stu-id="c67e1-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="c67e1-113">Beispiel 3: Starten einer Compliance-Überprüfung und Warten, bis sie im Hintergrund abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="c67e1-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="c67e1-114">Mit diesem Befehl wird eine Richtlinienkonformitätsauswertung für das aktive Abonnement gestartet.</span><span class="sxs-lookup"><span data-stu-id="c67e1-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="c67e1-115">Sie wartet, bis die Überprüfung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c67e1-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="c67e1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c67e1-116">PARAMETERS</span></span>

### <span data-ttu-id="c67e1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c67e1-117">-AsJob</span></span>
<span data-ttu-id="c67e1-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="c67e1-118">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c67e1-119">-DefaultProfile</span></span>
<span data-ttu-id="c67e1-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c67e1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67e1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c67e1-121">-PassThru</span></span>
<span data-ttu-id="c67e1-122">Gibt "True" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c67e1-122">Return True if the command completes successfully.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c67e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="c67e1-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c67e1-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c67e1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c67e1-125">-Confirm</span></span>
<span data-ttu-id="c67e1-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c67e1-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67e1-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c67e1-127">-WhatIf</span></span>
<span data-ttu-id="c67e1-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c67e1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c67e1-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c67e1-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c67e1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c67e1-130">CommonParameters</span></span>
<span data-ttu-id="c67e1-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c67e1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c67e1-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c67e1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c67e1-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c67e1-133">INPUTS</span></span>

### <span data-ttu-id="c67e1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c67e1-134">System.String</span></span>

## <span data-ttu-id="c67e1-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c67e1-135">OUTPUTS</span></span>

### <span data-ttu-id="c67e1-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c67e1-136">System.Boolean</span></span>

## <span data-ttu-id="c67e1-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c67e1-137">NOTES</span></span>

## <span data-ttu-id="c67e1-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c67e1-138">RELATED LINKS</span></span>
