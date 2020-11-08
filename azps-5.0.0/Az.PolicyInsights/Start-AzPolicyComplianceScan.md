---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177074"
---
# <span data-ttu-id="236fd-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="236fd-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="236fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="236fd-102">SYNOPSIS</span></span>
<span data-ttu-id="236fd-103">Löst eine Richtlinien Konformitätsbewertung für alle Ressourcen in einem Abonnement oder einer Ressourcengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="236fd-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="236fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="236fd-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="236fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="236fd-105">DESCRIPTION</span></span>
<span data-ttu-id="236fd-106">Das Cmdlet **Start-AzPolicyComplianceScan** startet eine Richtlinien Konformitätsbewertung für ein Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="236fd-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="236fd-107">Für alle Ressourcen innerhalb dieses Bereichs wird der Konformitätsstatus für alle zugewiesenen Richtlinien ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="236fd-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="236fd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="236fd-108">EXAMPLES</span></span>

### <span data-ttu-id="236fd-109">Beispiel 1: Starten einer Konformitätsüberprüfung im Abonnement Bereich</span><span class="sxs-lookup"><span data-stu-id="236fd-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="236fd-110">Mit diesem Befehl wird eine Richtlinien Konformitätsbewertung für das aktive Abonnement gestartet.</span><span class="sxs-lookup"><span data-stu-id="236fd-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="236fd-111">Beispiel 2: Starten eines Konformitätsscans im Bereich der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="236fd-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="236fd-112">Mit diesem Befehl wird eine Richtlinien Konformitätsbewertung für die Ressourcengruppe "myRG" im aktiven Abonnement gestartet.</span><span class="sxs-lookup"><span data-stu-id="236fd-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="236fd-113">Beispiel 3: Starten eines Konformitätsscans und abwarten des Abschlusses im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="236fd-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="236fd-114">Mit diesem Befehl wird eine Richtlinien Konformitätsbewertung für das aktive Abonnement gestartet.</span><span class="sxs-lookup"><span data-stu-id="236fd-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="236fd-115">Der Vorgang wartet, bis die Überprüfung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="236fd-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="236fd-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="236fd-116">PARAMETERS</span></span>

### <span data-ttu-id="236fd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="236fd-117">-AsJob</span></span>
<span data-ttu-id="236fd-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="236fd-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="236fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236fd-119">-DefaultProfile</span></span>
<span data-ttu-id="236fd-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="236fd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="236fd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="236fd-121">-PassThru</span></span>
<span data-ttu-id="236fd-122">Gibt "true" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="236fd-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="236fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="236fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="236fd-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="236fd-124">Resource group name.</span></span>

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

### <span data-ttu-id="236fd-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="236fd-125">-Confirm</span></span>
<span data-ttu-id="236fd-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="236fd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="236fd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="236fd-127">-WhatIf</span></span>
<span data-ttu-id="236fd-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="236fd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="236fd-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="236fd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="236fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236fd-130">CommonParameters</span></span>
<span data-ttu-id="236fd-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="236fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236fd-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="236fd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236fd-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="236fd-133">INPUTS</span></span>

### <span data-ttu-id="236fd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="236fd-134">System.String</span></span>

## <span data-ttu-id="236fd-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="236fd-135">OUTPUTS</span></span>

### <span data-ttu-id="236fd-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="236fd-136">System.Boolean</span></span>

## <span data-ttu-id="236fd-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="236fd-137">NOTES</span></span>

## <span data-ttu-id="236fd-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="236fd-138">RELATED LINKS</span></span>
