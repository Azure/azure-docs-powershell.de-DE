---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178427"
---
# <span data-ttu-id="6106c-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6106c-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="6106c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6106c-102">SYNOPSIS</span></span>
<span data-ttu-id="6106c-103">Kopiert Daten aus einem Tresor in einer Region in einen Tresor in einem anderen Bereich.</span><span class="sxs-lookup"><span data-stu-id="6106c-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="6106c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6106c-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="6106c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6106c-105">DESCRIPTION</span></span>
<span data-ttu-id="6106c-106">Das Cmdlet **Copy-AzRecoveryServicesVault** kopiert Daten aus einem Tresor in einem Bereich in einen Tresor in einem anderen Bereich.</span><span class="sxs-lookup"><span data-stu-id="6106c-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="6106c-107">Derzeit unterstützen wir nur die Datenverschiebung auf Vault-Ebene.</span><span class="sxs-lookup"><span data-stu-id="6106c-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="6106c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6106c-108">EXAMPLES</span></span>

### <span data-ttu-id="6106c-109">Beispiel 1: Kopieren von Daten aus vault1 in vault2</span><span class="sxs-lookup"><span data-stu-id="6106c-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### <span data-ttu-id="6106c-110">-Force</span><span class="sxs-lookup"><span data-stu-id="6106c-110">-Force</span></span>
<span data-ttu-id="6106c-111">Erzwingt den Daten Verschiebevorgang (verhindert das Bestätigungsdialogfeld), ohne eine Bestätigung für den Typ des Speicherredundanz Typs für Vault zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6106c-111">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="6106c-112">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6106c-112">This parameter is optional.</span></span> 

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

### <span data-ttu-id="6106c-113">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="6106c-113">-RetryOnlyFailed</span></span>
<span data-ttu-id="6106c-114">Parameter wechseln, um zu versuchen, Daten nur für Container im Quell Tresor zu verschieben, die noch nicht verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="6106c-114">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="6106c-115">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="6106c-115">-SourceVault</span></span>
<span data-ttu-id="6106c-116">Das Quell Tresor-Objekt, das verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6106c-116">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="6106c-117">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="6106c-117">-TargetVault</span></span>
<span data-ttu-id="6106c-118">Das Ziel Tresor-Objekt, in das die Daten verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6106c-118">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="6106c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6106c-119">CommonParameters</span></span>
<span data-ttu-id="6106c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6106c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6106c-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6106c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6106c-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6106c-122">INPUTS</span></span>

### <span data-ttu-id="6106c-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="6106c-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6106c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6106c-124">OUTPUTS</span></span>

### <span data-ttu-id="6106c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6106c-125">System.String</span></span>

## <span data-ttu-id="6106c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6106c-126">NOTES</span></span>

## <span data-ttu-id="6106c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6106c-127">RELATED LINKS</span></span>
