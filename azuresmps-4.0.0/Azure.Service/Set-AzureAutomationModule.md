---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006036"
---
# <span data-ttu-id="9b8e6-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9b8e6-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="9b8e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b8e6-102">SYNOPSIS</span></span>

<span data-ttu-id="9b8e6-103">Aktualisiert ein Modul in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="9b8e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b8e6-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b8e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b8e6-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9b8e6-106">Das Cmdlet " **Satz-AzureAutomationModule** " importiert eine neue Version eines Moduls oder ändert die Konfiguration des Moduls in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="9b8e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b8e6-107">EXAMPLES</span></span>

### <span data-ttu-id="9b8e6-108">Beispiel 1: Aktualisieren eines Moduls</span><span class="sxs-lookup"><span data-stu-id="9b8e6-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="9b8e6-109">Dieser Befehl importiert eine aktualisierte Version eines vorhandenen Moduls mit dem Namen ContosoModule in das Azure-Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9b8e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b8e6-110">PARAMETERS</span></span>

### <span data-ttu-id="9b8e6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9b8e6-111">-AutomationAccountName</span></span>
<span data-ttu-id="9b8e6-112">Gibt den Namen des Automatisierungs Kontos mit dem Modul an.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="9b8e6-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="9b8e6-113">-ContentLinkUri</span></span>
<span data-ttu-id="9b8e6-114">Gibt den Pfad zur Moduldatei an.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8e6-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="9b8e6-115">-ContentLinkVersion</span></span>
<span data-ttu-id="9b8e6-116">Gibt die Version des Moduls an.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-116">Specifies the version of the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8e6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9b8e6-117">-Name</span></span>
<span data-ttu-id="9b8e6-118">Gibt den Namen des Moduls an.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="9b8e6-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="9b8e6-119">-Profile</span></span>
<span data-ttu-id="9b8e6-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b8e6-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b8e6-122">-Tags</span><span class="sxs-lookup"><span data-stu-id="9b8e6-122">-Tags</span></span>
<span data-ttu-id="9b8e6-123">Gibt Tags für das Modul an.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-123">Specifies tags for the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8e6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8e6-124">CommonParameters</span></span>
<span data-ttu-id="9b8e6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8e6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8e6-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b8e6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8e6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b8e6-127">INPUTS</span></span>

### <span data-ttu-id="9b8e6-128">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="9b8e6-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="9b8e6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b8e6-129">OUTPUTS</span></span>

## <span data-ttu-id="9b8e6-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b8e6-130">NOTES</span></span>

## <span data-ttu-id="9b8e6-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b8e6-131">RELATED LINKS</span></span>

[<span data-ttu-id="9b8e6-132">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9b8e6-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="9b8e6-133">Neu – AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9b8e6-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="9b8e6-134">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9b8e6-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)


