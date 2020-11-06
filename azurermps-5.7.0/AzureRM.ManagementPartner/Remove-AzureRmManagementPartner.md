---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393045
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
ms.openlocfilehash: 703c38d02ef6a6a339c58c861961cd2ad92ecb7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499829"
---
# <span data-ttu-id="933a6-101">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="933a6-101">Remove-AzureRmManagementPartner</span></span>

## <span data-ttu-id="933a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="933a6-102">SYNOPSIS</span></span>
<span data-ttu-id="933a6-103">Löschen Sie die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="933a6-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="933a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="933a6-104">SYNTAX</span></span>

```
Remove-AzureRmManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="933a6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="933a6-105">DESCRIPTION</span></span>
<span data-ttu-id="933a6-106">Löschen Sie die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="933a6-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="933a6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="933a6-107">EXAMPLES</span></span>

### <span data-ttu-id="933a6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="933a6-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzureRmManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="933a6-109">VERWALTUNGSPARTNER entfernen</span><span class="sxs-lookup"><span data-stu-id="933a6-109">Remove management partner</span></span> 

## <span data-ttu-id="933a6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="933a6-110">PARAMETERS</span></span>

### <span data-ttu-id="933a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="933a6-111">-DefaultProfile</span></span>
<span data-ttu-id="933a6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="933a6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="933a6-113">-Partner-Nr</span><span class="sxs-lookup"><span data-stu-id="933a6-113">-PartnerId</span></span>
<span data-ttu-id="933a6-114">Die VERWALTUNGSPARTNER-ID ist eine sechsstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="933a6-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="933a6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="933a6-115">-PassThru</span></span>
<span data-ttu-id="933a6-116">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="933a6-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="933a6-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="933a6-117">-Confirm</span></span>
<span data-ttu-id="933a6-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="933a6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="933a6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="933a6-119">-WhatIf</span></span>
<span data-ttu-id="933a6-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="933a6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="933a6-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="933a6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="933a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933a6-122">CommonParameters</span></span>
<span data-ttu-id="933a6-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="933a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933a6-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="933a6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933a6-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="933a6-125">INPUTS</span></span>

### <span data-ttu-id="933a6-126">Keine</span><span class="sxs-lookup"><span data-stu-id="933a6-126">None</span></span>

## <span data-ttu-id="933a6-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="933a6-127">OUTPUTS</span></span>

### <span data-ttu-id="933a6-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="933a6-128">System.Object</span></span>

## <span data-ttu-id="933a6-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="933a6-129">NOTES</span></span>

## <span data-ttu-id="933a6-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="933a6-130">RELATED LINKS</span></span>

[<span data-ttu-id="933a6-131">Neu – AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="933a6-131">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="933a6-132">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="933a6-132">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="933a6-133">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="933a6-133">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
