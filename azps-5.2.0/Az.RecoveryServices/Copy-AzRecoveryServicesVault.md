---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 68c2914c694dbfb89044597fc35582a83f426b6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298843"
---
# <span data-ttu-id="b5517-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b5517-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b5517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5517-102">SYNOPSIS</span></span>
<span data-ttu-id="b5517-103">Kopiert Daten aus einem Tresor in einer Region in einen Tresor in einer anderen Region.</span><span class="sxs-lookup"><span data-stu-id="b5517-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="b5517-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5517-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="b5517-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5517-105">DESCRIPTION</span></span>
<span data-ttu-id="b5517-106">Das **Cmdlet "Copy-AzRecoveryServicesVault"** kopiert Daten aus einem Tresor in einer Region in einen Tresor in einer anderen Region.</span><span class="sxs-lookup"><span data-stu-id="b5517-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="b5517-107">Derzeit wird nur das Verschieben von Daten auf Tresorebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5517-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="b5517-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5517-108">EXAMPLES</span></span>

### <span data-ttu-id="b5517-109">Beispiel 1: Kopieren von Daten aus Tresor1 in Tresor2</span><span class="sxs-lookup"><span data-stu-id="b5517-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="b5517-110">Die ersten beiden Cmdlets rufen den Wiederherstellungsdiensttresor ab – Tresor1 bzw. Tresor2.</span><span class="sxs-lookup"><span data-stu-id="b5517-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="b5517-111">Der zweite Befehl löst eine vollständige Datenverwaltung vom Tresor1 in den Tresor2 aus.</span><span class="sxs-lookup"><span data-stu-id="b5517-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="b5517-112">Beispiel 2: Kopieren von Daten aus Tresor1 in Tresor2 mit nur fehlgeschlagenen Elementen</span><span class="sxs-lookup"><span data-stu-id="b5517-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
``` 

<span data-ttu-id="b5517-113">Die ersten beiden Cmdlets rufen den Wiederherstellungsdiensttresor ab – Tresor1 bzw. Tresor2.</span><span class="sxs-lookup"><span data-stu-id="b5517-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="b5517-114">Der zweite Befehl löst eine Teilweise Datenver verschiebung aus Tresor1 in Tresor2 mit nur den Elementen aus, bei denen bei vorherigen Verschiebevorgängen ein Fehler aufting.</span><span class="sxs-lookup"><span data-stu-id="b5517-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="b5517-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5517-115">PARAMETERS</span></span>

### <span data-ttu-id="b5517-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5517-116">-DefaultProfile</span></span>
<span data-ttu-id="b5517-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5517-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5517-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b5517-118">-Force</span></span>
<span data-ttu-id="b5517-119">Erzwingt den Datendatenübertragungsvorgang (verhindert ein Bestätigungsdialogfeld), ohne eine Bestätigung für den Speicherredundanztyp des Zieltresor an bitten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="b5517-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="b5517-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b5517-120">This parameter is optional.</span></span> 

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

### <span data-ttu-id="b5517-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="b5517-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="b5517-122">Wechseln Sie den Parameter, um das Verschieben von Daten nur für Container im Quelltresor auszuprobieren, die noch nicht verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="b5517-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="b5517-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="b5517-123">-SourceVault</span></span>
<span data-ttu-id="b5517-124">Das zu verschobene Quelltresorobjekt.</span><span class="sxs-lookup"><span data-stu-id="b5517-124">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5517-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="b5517-125">-TargetVault</span></span>
<span data-ttu-id="b5517-126">Das Zieltresorobjekt, in das die Daten verschoben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b5517-126">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5517-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5517-127">CommonParameters</span></span>
<span data-ttu-id="b5517-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5517-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5517-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5517-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5517-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5517-130">INPUTS</span></span>

### <span data-ttu-id="b5517-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="b5517-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b5517-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5517-132">OUTPUTS</span></span>

### <span data-ttu-id="b5517-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b5517-133">System.String</span></span>

## <span data-ttu-id="b5517-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b5517-134">NOTES</span></span>

## <span data-ttu-id="b5517-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b5517-135">RELATED LINKS</span></span>
