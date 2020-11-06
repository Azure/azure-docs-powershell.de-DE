---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: 9a6d6d0d21a38ac5ff41460021287e0701de6057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500541"
---
# <span data-ttu-id="78770-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="78770-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="78770-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78770-102">SYNOPSIS</span></span>
<span data-ttu-id="78770-103">Ordnet dem aktuell authentifizierten Benutzer oder Dienstprinzipal eine Microsoft Partner Network (MPN)-ID zu.</span><span class="sxs-lookup"><span data-stu-id="78770-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78770-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78770-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78770-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78770-105">DESCRIPTION</span></span>
<span data-ttu-id="78770-106">Ordnet dem aktuell authentifizierten Benutzer oder Dienstprinzipal eine Microsoft Partner Network (MPN)-ID zu.</span><span class="sxs-lookup"><span data-stu-id="78770-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="78770-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78770-107">EXAMPLES</span></span>

### <span data-ttu-id="78770-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78770-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="78770-109">Hinzufügen eines Verwaltungs Partners</span><span class="sxs-lookup"><span data-stu-id="78770-109">Add a management partner</span></span> 

## <span data-ttu-id="78770-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="78770-110">PARAMETERS</span></span>

### <span data-ttu-id="78770-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78770-111">-DefaultProfile</span></span>
<span data-ttu-id="78770-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78770-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78770-113">-Partner-Nr</span><span class="sxs-lookup"><span data-stu-id="78770-113">-PartnerId</span></span>
<span data-ttu-id="78770-114">Die VERWALTUNGSPARTNER-ID ist eine sechsstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="78770-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78770-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78770-115">-Confirm</span></span>
<span data-ttu-id="78770-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78770-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78770-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78770-117">-WhatIf</span></span>
<span data-ttu-id="78770-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78770-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78770-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78770-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78770-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78770-120">CommonParameters</span></span>
<span data-ttu-id="78770-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78770-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78770-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78770-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78770-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78770-123">INPUTS</span></span>

### <span data-ttu-id="78770-124">Keine</span><span class="sxs-lookup"><span data-stu-id="78770-124">None</span></span>

## <span data-ttu-id="78770-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78770-125">OUTPUTS</span></span>

### <span data-ttu-id="78770-126">Microsoft. Azure. Commands. resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="78770-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="78770-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="78770-127">NOTES</span></span>

## <span data-ttu-id="78770-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78770-128">RELATED LINKS</span></span>

[<span data-ttu-id="78770-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="78770-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="78770-130">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="78770-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="78770-131">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="78770-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
