---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005700"
---
# <span data-ttu-id="59ed5-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="59ed5-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="59ed5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="59ed5-103">Entfernt eine Azure Virtual Machine-SQL Server-Erweiterung von einem virtuellen Computerobjekt.</span><span class="sxs-lookup"><span data-stu-id="59ed5-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="59ed5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59ed5-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="59ed5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="59ed5-106">Das Cmdlet **Remove-AzureVMSqlServerExtension** entfernt eine Azure Virtual Machine-SQL Server-Erweiterung von einem virtuellen Computerobjekt.</span><span class="sxs-lookup"><span data-stu-id="59ed5-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="59ed5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59ed5-107">EXAMPLES</span></span>

### <span data-ttu-id="59ed5-108">1:</span><span class="sxs-lookup"><span data-stu-id="59ed5-108">1:</span></span>
```

```

## <span data-ttu-id="59ed5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="59ed5-109">PARAMETERS</span></span>

### <span data-ttu-id="59ed5-110">-Information</span><span class="sxs-lookup"><span data-stu-id="59ed5-110">-InformationAction</span></span>
<span data-ttu-id="59ed5-111">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="59ed5-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="59ed5-112">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="59ed5-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59ed5-113">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="59ed5-113">Continue</span></span>
- <span data-ttu-id="59ed5-114">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="59ed5-114">Ignore</span></span>
- <span data-ttu-id="59ed5-115">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="59ed5-115">Inquire</span></span>
- <span data-ttu-id="59ed5-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="59ed5-116">SilentlyContinue</span></span>
- <span data-ttu-id="59ed5-117">Beenden</span><span class="sxs-lookup"><span data-stu-id="59ed5-117">Stop</span></span>
- <span data-ttu-id="59ed5-118">Anhalten</span><span class="sxs-lookup"><span data-stu-id="59ed5-118">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ed5-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="59ed5-119">-InformationVariable</span></span>
<span data-ttu-id="59ed5-120">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="59ed5-120">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ed5-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="59ed5-121">-Profile</span></span>
<span data-ttu-id="59ed5-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="59ed5-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="59ed5-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="59ed5-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ed5-124">-VM</span><span class="sxs-lookup"><span data-stu-id="59ed5-124">-VM</span></span>
<span data-ttu-id="59ed5-125">Gibt das Objekt des beständigen virtuellen Computers an, von dem dieses Cmdlet die Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="59ed5-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59ed5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ed5-126">CommonParameters</span></span>
<span data-ttu-id="59ed5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59ed5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ed5-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ed5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ed5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59ed5-129">INPUTS</span></span>

## <span data-ttu-id="59ed5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59ed5-130">OUTPUTS</span></span>

## <span data-ttu-id="59ed5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="59ed5-131">NOTES</span></span>

## <span data-ttu-id="59ed5-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59ed5-132">RELATED LINKS</span></span>

[<span data-ttu-id="59ed5-133">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="59ed5-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="59ed5-134">Satz-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="59ed5-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


