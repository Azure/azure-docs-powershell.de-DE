---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006076"
---
# <span data-ttu-id="243ba-101">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="243ba-101">Remove-AzureAccount</span></span>

## <span data-ttu-id="243ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="243ba-102">SYNOPSIS</span></span>
<span data-ttu-id="243ba-103">Löscht ein Azure-Konto aus Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="243ba-103">Deletes an Azure account from Windows PowerShell.</span></span>

## <span data-ttu-id="243ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="243ba-104">SYNTAX</span></span>

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="243ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="243ba-105">DESCRIPTION</span></span>
<span data-ttu-id="243ba-106">Das Cmdlet **Remove-AzureAccount** löscht ein Azure-Konto und seine Abonnements aus der Abonnement Datendatei in Ihrem Roaming-Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="243ba-106">The **Remove-AzureAccount** cmdlet deletes an Azure account and its subscriptions from the subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="243ba-107">Dadurch wird das Konto nicht aus Microsoft Azure gelöscht oder das tatsächliche Konto in irgendeiner Weise geändert.</span><span class="sxs-lookup"><span data-stu-id="243ba-107">It does not delete the account from Microsoft Azure, or change the actual account in any way.</span></span>

<span data-ttu-id="243ba-108">Die Verwendung dieses Cmdlets ähnelt viel dem Abmelden von Ihrem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="243ba-108">Using this cmdlet is a lot like logging out of your Azure account.</span></span>
<span data-ttu-id="243ba-109">Wenn Sie sich erneut bei dem Konto anmelden möchten, verwenden Sie das **Add-AzureAccount** oder **Import-AzurePublishSettingsFile** , um das Konto erneut zu Windows PowerShell hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="243ba-109">And, if you want to log into the account again, use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** to add the account to Windows PowerShell again.</span></span>

<span data-ttu-id="243ba-110">Sie können auch das Cmdlet **Remove-AzureAccount** verwenden, um die Art und Weise zu ändern, wie sich die Azure PowerShell-Cmdlets bei Ihrem Azure-Konto anmelden.</span><span class="sxs-lookup"><span data-stu-id="243ba-110">You can also use **Remove-AzureAccount** cmdlet to change the way the Azure PowerShell cmdlets sign into your Azure account.</span></span>
<span data-ttu-id="243ba-111">Wenn Ihr Konto über ein Verwaltungszertifikat von **Import-AzurePublishSettingsFile** und ein Zugriffstoken von **Add-AzureAccount** verfügt, verwenden die Azure PowerShell-Cmdlets nur das Zugriffstoken; Das Verwaltungszertifikat wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="243ba-111">If your account has both a management certificate from **Import-AzurePublishSettingsFile** and an access token from **Add-AzureAccount** , the Azure PowerShell cmdlets use only the access token; they ignore the management certificate.</span></span>
<span data-ttu-id="243ba-112">Wenn Sie das Verwaltungszertifikat verwenden möchten, führen **Sie Remove-AzureAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="243ba-112">To use the management certificate, run **Remove-AzureAccount**.</span></span>
<span data-ttu-id="243ba-113">Wenn **Remove-AzureAccount** sowohl ein Verwaltungszertifikat als auch ein Zugriffstoken findet, wird nur das Zugriffstoken gelöscht, anstatt das Konto zu löschen.</span><span class="sxs-lookup"><span data-stu-id="243ba-113">When **Remove-AzureAccount** finds both a management certificate and an access token, it deletes only the access token, instead of deleting the account.</span></span>
<span data-ttu-id="243ba-114">Da das Verwaltungszertifikat weiterhin vorhanden ist, steht das Konto weiterhin für Windows PowerShell zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="243ba-114">The management certificate is still there, so account is still available to Windows PowerShell.</span></span>

<span data-ttu-id="243ba-115">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="243ba-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="243ba-116">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="243ba-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="243ba-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="243ba-117">EXAMPLES</span></span>

### <span data-ttu-id="243ba-118">Beispiel 1: Entfernen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="243ba-118">Example 1: Remove an account</span></span>
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

<span data-ttu-id="243ba-119">Mit diesem Befehl wird die admin@contoso.com aus der Abonnement Datendatei entfernte Datei entfernt.</span><span class="sxs-lookup"><span data-stu-id="243ba-119">This command removes the admin@contoso.com from your subscription data file.</span></span>
<span data-ttu-id="243ba-120">Nach Abschluss des Befehls steht das Konto nicht mehr für Windows PowerShell zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="243ba-120">When the command completes, the account is no longer available to Windows PowerShell.</span></span>

## <span data-ttu-id="243ba-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="243ba-121">PARAMETERS</span></span>

### <span data-ttu-id="243ba-122">-Force</span><span class="sxs-lookup"><span data-stu-id="243ba-122">-Force</span></span>
<span data-ttu-id="243ba-123">Unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="243ba-123">Suppresses the confirmation prompt.</span></span>
<span data-ttu-id="243ba-124">Standardmäßig werden Sie von **Remove-AzureAccount** aufgefordert, bevor Sie das Konto aus Windows PowerShell entfernen.</span><span class="sxs-lookup"><span data-stu-id="243ba-124">By default, **Remove-AzureAccount** prompts you before removing the account from Windows PowerShell.</span></span>

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

### <span data-ttu-id="243ba-125">-Name</span><span class="sxs-lookup"><span data-stu-id="243ba-125">-Name</span></span>
<span data-ttu-id="243ba-126">Gibt den Namen des zu entfernenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="243ba-126">Specifies the name of the account to remove.</span></span>
<span data-ttu-id="243ba-127">Bei dem Parameterwert wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="243ba-127">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="243ba-128">Platzhalterzeichen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="243ba-128">Wildcard characters are not supported.</span></span>

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

### <span data-ttu-id="243ba-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="243ba-129">-PassThru</span></span>
<span data-ttu-id="243ba-130">Gibt $true zurück, wenn der Befehl erfolgreich ist, und $false, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="243ba-130">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="243ba-131">Standardmäßig gibt dieses Cmdlet keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="243ba-131">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="243ba-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="243ba-132">-Profile</span></span>
<span data-ttu-id="243ba-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="243ba-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="243ba-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="243ba-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="243ba-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="243ba-135">-Confirm</span></span>
<span data-ttu-id="243ba-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="243ba-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="243ba-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="243ba-137">-WhatIf</span></span>
<span data-ttu-id="243ba-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="243ba-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="243ba-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="243ba-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="243ba-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243ba-140">CommonParameters</span></span>
<span data-ttu-id="243ba-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="243ba-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243ba-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="243ba-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243ba-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="243ba-143">INPUTS</span></span>

### <span data-ttu-id="243ba-144">Keine</span><span class="sxs-lookup"><span data-stu-id="243ba-144">None</span></span>
<span data-ttu-id="243ba-145">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="243ba-145">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="243ba-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="243ba-146">OUTPUTS</span></span>

### <span data-ttu-id="243ba-147">None oder System. Boolean</span><span class="sxs-lookup"><span data-stu-id="243ba-147">None or System.Boolean</span></span>
<span data-ttu-id="243ba-148">Wenn Sie den Parameter *passthru* verwenden, gibt dieses Cmdlet einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="243ba-148">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="243ba-149">Andernfalls gibt Sie keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="243ba-149">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="243ba-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="243ba-150">NOTES</span></span>

## <span data-ttu-id="243ba-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="243ba-151">RELATED LINKS</span></span>

[<span data-ttu-id="243ba-152">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="243ba-152">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="243ba-153">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="243ba-153">Get-AzureAccount</span></span>](./Get-AzureAccount.md)


