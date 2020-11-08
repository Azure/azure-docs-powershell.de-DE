---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006301"
---
# <span data-ttu-id="04f80-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="04f80-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="04f80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04f80-102">SYNOPSIS</span></span>
<span data-ttu-id="04f80-103">Löscht ein Azure-Abonnement aus Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04f80-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="04f80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04f80-104">SYNTAX</span></span>

### <span data-ttu-id="04f80-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="04f80-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f80-106">ID</span><span class="sxs-lookup"><span data-stu-id="04f80-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04f80-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04f80-107">DESCRIPTION</span></span>
<span data-ttu-id="04f80-108">Das Cmdlet **Remove-AzureSubscription** löscht ein Azure-Abonnement aus ihrer Abonnementdaten Datei, damit es von Windows PowerShell nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="04f80-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="04f80-109">Mit diesem Cmdlet wird das Abonnement nicht von Microsoft Azure gelöscht oder das tatsächliche Abonnement in irgendeiner Weise geändert.</span><span class="sxs-lookup"><span data-stu-id="04f80-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="04f80-110">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="04f80-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="04f80-111">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="04f80-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="04f80-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04f80-112">EXAMPLES</span></span>

### <span data-ttu-id="04f80-113">Beispiel 1: Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="04f80-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="04f80-114">Dieser Befehl löscht das "Test"-Abonnement aus der Standarddaten Datei des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="04f80-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="04f80-115">Beispiel 2: Löschen aus einer alternativen Abonnement Datendatei</span><span class="sxs-lookup"><span data-stu-id="04f80-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="04f80-116">Dieser Befehl löscht das Test Abonnement aus der MySubscriptions.xml-Abonnement Datendatei.</span><span class="sxs-lookup"><span data-stu-id="04f80-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="04f80-117">Der Befehl verwendet den *Force* -Parameter, um die Bestätigungsaufforderung zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="04f80-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="04f80-118">Beispiel 3: Löschen eines Abonnements in einem Skript</span><span class="sxs-lookup"><span data-stu-id="04f80-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="04f80-119">Dieser Befehl verwendet den Befehl **Remove-AzureSubscription** in einer **if** -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="04f80-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="04f80-120">Es wird der *passthru* -Parameter verwendet, der einen booleschen Wert zurückgibt, um zu ermitteln, ob der Skriptblock in der **if** -Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04f80-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="04f80-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="04f80-121">PARAMETERS</span></span>

### <span data-ttu-id="04f80-122">-Force</span><span class="sxs-lookup"><span data-stu-id="04f80-122">-Force</span></span>
<span data-ttu-id="04f80-123">Unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="04f80-123">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="04f80-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04f80-124">-PassThru</span></span>
<span data-ttu-id="04f80-125">Gibt $true zurück, wenn der Befehl erfolgreich ist, und $false, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="04f80-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="04f80-126">Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="04f80-126">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="04f80-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="04f80-127">-Profile</span></span>
<span data-ttu-id="04f80-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="04f80-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="04f80-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="04f80-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04f80-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="04f80-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f80-131">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="04f80-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f80-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04f80-132">-Confirm</span></span>
<span data-ttu-id="04f80-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04f80-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f80-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f80-134">-WhatIf</span></span>
<span data-ttu-id="04f80-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04f80-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04f80-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04f80-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f80-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f80-137">CommonParameters</span></span>
<span data-ttu-id="04f80-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04f80-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f80-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04f80-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f80-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04f80-140">INPUTS</span></span>

### <span data-ttu-id="04f80-141">Keine</span><span class="sxs-lookup"><span data-stu-id="04f80-141">None</span></span>
<span data-ttu-id="04f80-142">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="04f80-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="04f80-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04f80-143">OUTPUTS</span></span>

### <span data-ttu-id="04f80-144">None oder System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04f80-144">None or System.Boolean</span></span>
<span data-ttu-id="04f80-145">Wenn Sie den Parameter *passthru* verwenden, gibt dieses Cmdlet einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="04f80-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="04f80-146">Andernfalls gibt Sie keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="04f80-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="04f80-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="04f80-147">NOTES</span></span>

## <span data-ttu-id="04f80-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04f80-148">RELATED LINKS</span></span>

[<span data-ttu-id="04f80-149">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="04f80-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="04f80-150">SELECT-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="04f80-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="04f80-151">Satz-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="04f80-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


