---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: d9309f2de88dc87368b510cdf6f1062d03c7f709
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496558"
---
# <span data-ttu-id="fe2c0-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="fe2c0-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="fe2c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2c0-103">Erstellt ein neues Aktivitätsprotokoll-Warnungs Konditions Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe2c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe2c0-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe2c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe2c0-105">DESCRIPTION</span></span>
<span data-ttu-id="fe2c0-106">Das Cmdlet **New-AzureRmActivityLogAlertCondition** erstellt ein neues Aktivitätsprotokoll-Warnungs Bedingungsobjekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="fe2c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe2c0-107">EXAMPLES</span></span>

### <span data-ttu-id="fe2c0-108">Beispiel 1: Erstellen eines neuen Aktivitätsprotokoll-Warnungs Bedingungs Objekts im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="fe2c0-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="fe2c0-109">Dieser Befehl erstellt ein neues Aktivitätsprotokoll-Warnungs Konditions Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-109">This command creates a new activity log alert condition object in memory.</span></span>

<span data-ttu-id="fe2c0-110">**Hinweis** : Wenn dieses Cmdlet mit Set-AzureRmActivityLogAlert verwendet wird, muss mindestens eines dieser Objekte, das als Parameter übergeben wird, sein Feld gleich "Category" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="fe2c0-111">Andernfalls reagiert das Back-End mit einem 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="fe2c0-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="fe2c0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe2c0-112">PARAMETERS</span></span>

### <span data-ttu-id="fe2c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2c0-113">-DefaultProfile</span></span>
<span data-ttu-id="fe2c0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fe2c0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe2c0-115">-EQUAL</span><span class="sxs-lookup"><span data-stu-id="fe2c0-115">-Equal</span></span>
<span data-ttu-id="fe2c0-116">Gibt die Equals-Eigenschaft für die Blatt Bedingung an.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-116">Specifies the equals property for the leaf condition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2c0-117">-Field</span><span class="sxs-lookup"><span data-stu-id="fe2c0-117">-Field</span></span>
<span data-ttu-id="fe2c0-118">Gibt das Feld für die Bedingung an.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-118">Specifies the field for the condition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2c0-119">CommonParameters</span></span>
<span data-ttu-id="fe2c0-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2c0-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2c0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2c0-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe2c0-122">INPUTS</span></span>

### <span data-ttu-id="fe2c0-123">Keine</span><span class="sxs-lookup"><span data-stu-id="fe2c0-123">None</span></span>
<span data-ttu-id="fe2c0-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fe2c0-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe2c0-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe2c0-125">OUTPUTS</span></span>

### <span data-ttu-id="fe2c0-126">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="fe2c0-126">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="fe2c0-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe2c0-127">NOTES</span></span>

## <span data-ttu-id="fe2c0-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe2c0-128">RELATED LINKS</span></span>

[<span data-ttu-id="fe2c0-129">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe2c0-129">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fe2c0-130">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe2c0-130">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fe2c0-131">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe2c0-131">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fe2c0-132">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe2c0-132">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fe2c0-133">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="fe2c0-133">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="fe2c0-134">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="fe2c0-134">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
