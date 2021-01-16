---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297233"
---
# <span data-ttu-id="ea5da-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="ea5da-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="ea5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea5da-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5da-103">Gibt die BitLocker-Schlüssel für alle Laufwerke im angegebenen Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="ea5da-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="ea5da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea5da-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ea5da-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea5da-105">DESCRIPTION</span></span>
<span data-ttu-id="ea5da-106">Gibt die BitLocker Keys für alle Laufwerke im angegebenen Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="ea5da-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="ea5da-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea5da-107">EXAMPLES</span></span>

### <span data-ttu-id="ea5da-108">Beispiel 1: Auflisten aller BitLocker-Schlüssel im angegebenen ImportExport-Auftrag</span><span class="sxs-lookup"><span data-stu-id="ea5da-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="ea5da-109">Dieses Cmdlet listet alle BitLocker-Schlüssel im angegebenen ImportExport-Auftrag auf.</span><span class="sxs-lookup"><span data-stu-id="ea5da-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="ea5da-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea5da-110">PARAMETERS</span></span>

### <span data-ttu-id="ea5da-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="ea5da-111">-AcceptLanguage</span></span>
<span data-ttu-id="ea5da-112">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="ea5da-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="ea5da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5da-113">-DefaultProfile</span></span>
<span data-ttu-id="ea5da-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea5da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea5da-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="ea5da-115">-JobName</span></span>
<span data-ttu-id="ea5da-116">Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="ea5da-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="ea5da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5da-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea5da-118">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ea5da-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="ea5da-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea5da-119">-SubscriptionId</span></span>
<span data-ttu-id="ea5da-120">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ea5da-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="ea5da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5da-121">CommonParameters</span></span>
<span data-ttu-id="ea5da-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea5da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5da-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea5da-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5da-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea5da-124">INPUTS</span></span>

## <span data-ttu-id="ea5da-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea5da-125">OUTPUTS</span></span>

### <span data-ttu-id="ea5da-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="ea5da-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="ea5da-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea5da-127">NOTES</span></span>

<span data-ttu-id="ea5da-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ea5da-128">ALIASES</span></span>

## <span data-ttu-id="ea5da-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea5da-129">RELATED LINKS</span></span>

