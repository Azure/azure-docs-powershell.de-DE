---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844819"
---
# <span data-ttu-id="9467c-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="9467c-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="9467c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9467c-102">SYNOPSIS</span></span>


## <span data-ttu-id="9467c-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="9467c-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9467c-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9467c-104">DESCRIPTION</span></span>


## <span data-ttu-id="9467c-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9467c-105">EXAMPLES</span></span>

### <span data-ttu-id="9467c-106">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="9467c-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="9467c-107">Aktualisieren Sie die Speichereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="9467c-107">Update the storage settings.</span></span>

## <span data-ttu-id="9467c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9467c-108">PARAMETERS</span></span>

### <span data-ttu-id="9467c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9467c-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="9467c-110">-Force</span><span class="sxs-lookup"><span data-stu-id="9467c-110">-Force</span></span>


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

### <span data-ttu-id="9467c-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="9467c-111">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9467c-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="9467c-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9467c-113">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9467c-113">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9467c-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9467c-114">-Confirm</span></span>
<span data-ttu-id="9467c-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9467c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9467c-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9467c-116">-WhatIf</span></span>
<span data-ttu-id="9467c-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9467c-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9467c-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9467c-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9467c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9467c-119">CommonParameters</span></span>
<span data-ttu-id="9467c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9467c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9467c-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9467c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9467c-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9467c-122">INPUTS</span></span>

## <span data-ttu-id="9467c-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9467c-123">OUTPUTS</span></span>

### <span data-ttu-id="9467c-124">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="9467c-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="9467c-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="9467c-125">NOTES</span></span>

## <span data-ttu-id="9467c-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9467c-126">RELATED LINKS</span></span>

