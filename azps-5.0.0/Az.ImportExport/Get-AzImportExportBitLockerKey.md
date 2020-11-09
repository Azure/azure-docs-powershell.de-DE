---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296247"
---
# <span data-ttu-id="cd7db-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="cd7db-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="cd7db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd7db-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7db-103">Gibt die BitLocker-Schlüssel für alle Laufwerke des angegebenen Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="cd7db-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="cd7db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd7db-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cd7db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd7db-105">DESCRIPTION</span></span>
<span data-ttu-id="cd7db-106">Gibt die BitLocker-Schlüssel für alle Laufwerke des angegebenen Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="cd7db-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="cd7db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd7db-107">EXAMPLES</span></span>

### <span data-ttu-id="cd7db-108">Beispiel 1: Auflisten aller BitLocker-Schlüssel in angegebenen DataObjects-Aufträgen</span><span class="sxs-lookup"><span data-stu-id="cd7db-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="cd7db-109">Dieses Cmdlet listet alle BitLocker-Schlüssel in angegebenen DataObjects-Aufträgen auf.</span><span class="sxs-lookup"><span data-stu-id="cd7db-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="cd7db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd7db-110">PARAMETERS</span></span>

### <span data-ttu-id="cd7db-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="cd7db-111">-AcceptLanguage</span></span>
<span data-ttu-id="cd7db-112">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="cd7db-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="cd7db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7db-113">-DefaultProfile</span></span>
<span data-ttu-id="cd7db-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd7db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd7db-115">-Jobname</span><span class="sxs-lookup"><span data-stu-id="cd7db-115">-JobName</span></span>
<span data-ttu-id="cd7db-116">Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="cd7db-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="cd7db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7db-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd7db-118">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="cd7db-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="cd7db-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="cd7db-119">-SubscriptionId</span></span>
<span data-ttu-id="cd7db-120">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="cd7db-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="cd7db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7db-121">CommonParameters</span></span>
<span data-ttu-id="cd7db-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd7db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7db-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd7db-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7db-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd7db-124">INPUTS</span></span>

## <span data-ttu-id="cd7db-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd7db-125">OUTPUTS</span></span>

### <span data-ttu-id="cd7db-126">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. Api20161101. IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="cd7db-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="cd7db-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd7db-127">NOTES</span></span>

<span data-ttu-id="cd7db-128">Aliase</span><span class="sxs-lookup"><span data-stu-id="cd7db-128">ALIASES</span></span>

## <span data-ttu-id="cd7db-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd7db-129">RELATED LINKS</span></span>

