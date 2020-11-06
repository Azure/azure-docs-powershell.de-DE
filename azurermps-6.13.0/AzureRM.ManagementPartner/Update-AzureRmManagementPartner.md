---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 420353d7a8af1046456138918092ca56d5c6ed96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497362"
---
# <span data-ttu-id="0779b-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0779b-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="0779b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0779b-102">SYNOPSIS</span></span>
<span data-ttu-id="0779b-103">Aktualisiert die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="0779b-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0779b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0779b-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0779b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0779b-105">DESCRIPTION</span></span>
<span data-ttu-id="0779b-106">Aktualisiert die Microsoft Partner Network (MPN)-ID des aktuellen authentifizierten Benutzers oder Dienst Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="0779b-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0779b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0779b-107">EXAMPLES</span></span>

### <span data-ttu-id="0779b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0779b-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0779b-109">Aktualisieren des Verwaltungs Partners auf eine neue Version</span><span class="sxs-lookup"><span data-stu-id="0779b-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="0779b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0779b-110">PARAMETERS</span></span>

### <span data-ttu-id="0779b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0779b-111">-DefaultProfile</span></span>
<span data-ttu-id="0779b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0779b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779b-113">-Partner-Nr</span><span class="sxs-lookup"><span data-stu-id="0779b-113">-PartnerId</span></span>
<span data-ttu-id="0779b-114">Die VERWALTUNGSPARTNER-ID ist eine sechsstellige Zahl</span><span class="sxs-lookup"><span data-stu-id="0779b-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779b-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0779b-115">-Confirm</span></span>
<span data-ttu-id="0779b-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0779b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0779b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0779b-117">-WhatIf</span></span>
<span data-ttu-id="0779b-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0779b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0779b-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0779b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0779b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0779b-120">CommonParameters</span></span>
<span data-ttu-id="0779b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0779b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0779b-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0779b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0779b-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0779b-123">INPUTS</span></span>

### <span data-ttu-id="0779b-124">Keine</span><span class="sxs-lookup"><span data-stu-id="0779b-124">None</span></span>

## <span data-ttu-id="0779b-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0779b-125">OUTPUTS</span></span>

### <span data-ttu-id="0779b-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0779b-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="0779b-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="0779b-127">NOTES</span></span>

## <span data-ttu-id="0779b-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0779b-128">RELATED LINKS</span></span>

[<span data-ttu-id="0779b-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0779b-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="0779b-130">Neu – AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0779b-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="0779b-131">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0779b-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
