---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: fefd529b00b88c20b3703e1bcecbbb88c72d52e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924115"
---
# <span data-ttu-id="81024-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="81024-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="81024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81024-102">SYNOPSIS</span></span>
<span data-ttu-id="81024-103">Gibt die BitLockertasten für alle Laufwerke im angegebenen Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="81024-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="81024-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81024-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="81024-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81024-105">DESCRIPTION</span></span>
<span data-ttu-id="81024-106">Gibt die BitLockertasten für alle Laufwerke im angegebenen Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="81024-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="81024-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81024-107">EXAMPLES</span></span>

### <span data-ttu-id="81024-108">Beispiel 1: Auflisten aller BitLockerschlüssel im angegebenen ImportExportauftrag</span><span class="sxs-lookup"><span data-stu-id="81024-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="81024-109">In diesem Cmdlet werden alle BitLocker-Schlüssel im angegebenen ImportExportauftrag aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="81024-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="81024-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="81024-110">PARAMETERS</span></span>

### <span data-ttu-id="81024-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="81024-111">-AcceptLanguage</span></span>
<span data-ttu-id="81024-112">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="81024-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81024-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81024-113">-DefaultProfile</span></span>
<span data-ttu-id="81024-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81024-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81024-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="81024-115">-JobName</span></span>
<span data-ttu-id="81024-116">Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="81024-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="81024-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81024-117">-ResourceGroupName</span></span>
<span data-ttu-id="81024-118">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="81024-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="81024-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81024-119">-SubscriptionId</span></span>
<span data-ttu-id="81024-120">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="81024-120">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81024-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81024-121">CommonParameters</span></span>
<span data-ttu-id="81024-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81024-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81024-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81024-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81024-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81024-124">INPUTS</span></span>

## <span data-ttu-id="81024-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81024-125">OUTPUTS</span></span>

### <span data-ttu-id="81024-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="81024-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="81024-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="81024-127">NOTES</span></span>

<span data-ttu-id="81024-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="81024-128">ALIASES</span></span>

## <span data-ttu-id="81024-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="81024-129">RELATED LINKS</span></span>

