---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007606"
---
# <span data-ttu-id="8dfe8-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="8dfe8-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="8dfe8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8dfe8-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfe8-103">Erstellt einen virtuellen Computer basierend auf einer Vorlage.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="8dfe8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dfe8-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8dfe8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8dfe8-105">DESCRIPTION</span></span>
<span data-ttu-id="8dfe8-106">Diese Themen sind veraltet und werden in Zukunft entfernt.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8dfe8-107">In diesem Thema wird das Cmdlet in der Version 0.8.1 des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8dfe8-108">Wenn Sie die Version des verwendeten Moduls ermitteln möchten, geben Sie aus der Azure PowerShell-Konsole ein `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8dfe8-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8dfe8-109">Das Cmdlet **New-WAPackQuickVM** erstellt einen virtuellen Computer basierend auf einer Vorlage.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="8dfe8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8dfe8-110">EXAMPLES</span></span>

### <span data-ttu-id="8dfe8-111">Beispiel 1: Erstellen eines virtuellen Computers auf Grundlage einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="8dfe8-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="8dfe8-112">Der erste Befehl erstellt ein **PSCredential** -Objekt und speichert es dann in der $Credentials-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="8dfe8-113">Das Cmdlet fordert Sie zur Eingabe eines Kontos und eines Kennworts auf.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="8dfe8-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="8dfe8-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="8dfe8-115">Der zweite Befehl ruft eine Vorlage mit dem Cmdlet **Get-WAPackVMTemplate** ab.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="8dfe8-116">Der Befehl gibt die ID einer Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="8dfe8-117">Der Befehl speichert das Vorlagenobjekt in der $TemplateID Variablen.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="8dfe8-118">Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen VirtualMachine023.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="8dfe8-119">Der Befehl basiert auf dem virtuellen Computer auf der Vorlage, die in $TemplateId gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="8dfe8-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="8dfe8-120">PARAMETERS</span></span>

### <span data-ttu-id="8dfe8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8dfe8-121">-Name</span></span>
<span data-ttu-id="8dfe8-122">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-122">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="8dfe8-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="8dfe8-123">-Profile</span></span>
<span data-ttu-id="8dfe8-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8dfe8-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8dfe8-126">-Vorlage</span><span class="sxs-lookup"><span data-stu-id="8dfe8-126">-Template</span></span>
<span data-ttu-id="8dfe8-127">Gibt eine Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-127">Specifies a template.</span></span>
<span data-ttu-id="8dfe8-128">Das Cmdlet erstellt einen virtuellen Computer basierend auf der von Ihnen angegebenen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="8dfe8-129">Verwenden Sie zum Abrufen eines Vorlagenobjekts das Cmdlet **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="8dfe8-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dfe8-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="8dfe8-130">-VMCredential</span></span>
<span data-ttu-id="8dfe8-131">Gibt die Anmeldeinformationen für das lokale Administrator Konto an.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="8dfe8-132">Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="8dfe8-133">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="8dfe8-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dfe8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfe8-134">CommonParameters</span></span>
<span data-ttu-id="8dfe8-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dfe8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfe8-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dfe8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfe8-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8dfe8-137">INPUTS</span></span>

## <span data-ttu-id="8dfe8-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8dfe8-138">OUTPUTS</span></span>

## <span data-ttu-id="8dfe8-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="8dfe8-139">NOTES</span></span>

## <span data-ttu-id="8dfe8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8dfe8-140">RELATED LINKS</span></span>

[<span data-ttu-id="8dfe8-141">Neu – WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8dfe8-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="8dfe8-142">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="8dfe8-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


