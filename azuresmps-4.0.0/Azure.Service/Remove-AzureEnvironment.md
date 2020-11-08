---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006683"
---
# <span data-ttu-id="d41de-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d41de-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="d41de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d41de-102">SYNOPSIS</span></span>
<span data-ttu-id="d41de-103">Löscht eine Azure-Umgebung aus Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d41de-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="d41de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d41de-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d41de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d41de-105">DESCRIPTION</span></span>
<span data-ttu-id="d41de-106">Das Cmdlet **Remove-AzureEnvironment** löscht eine Azure-Umgebung aus Ihrem Roaming-Profil, damit Sie von Windows PowerShell nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="d41de-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="d41de-107">Mit diesem Cmdlet wird die Umgebung nicht aus Microsoft Azure gelöscht, oder die tatsächliche Umgebung wird in keiner Weise geändert.</span><span class="sxs-lookup"><span data-stu-id="d41de-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="d41de-108">Eine Azure-Umgebung eine unabhängige Bereitstellung von Microsoft Azure, wie AzureCloud für Global Azure und AzureChinaCloud für Azure, betrieben von 21Vianet in China.</span><span class="sxs-lookup"><span data-stu-id="d41de-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="d41de-109">Sie können auch lokale Azure-Umgebungen mithilfe von Azure Pack und den WAPack-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="d41de-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="d41de-110">Weitere Informationen finden Sie unter [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d41de-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="d41de-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d41de-111">EXAMPLES</span></span>

### <span data-ttu-id="d41de-112">Beispiel 1: Löschen einer Umgebung</span><span class="sxs-lookup"><span data-stu-id="d41de-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="d41de-113">Dieser Befehl löscht die ContosoEnv-Umgebung aus Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d41de-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="d41de-114">Beispiel 2: Löschen mehrerer Umgebungen</span><span class="sxs-lookup"><span data-stu-id="d41de-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="d41de-115">Dieser Befehl löscht Umgebungen, deren Namen mit "Contoso" von Windows PowerShell beginnen.</span><span class="sxs-lookup"><span data-stu-id="d41de-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="d41de-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d41de-116">PARAMETERS</span></span>

### <span data-ttu-id="d41de-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d41de-117">-Force</span></span>
<span data-ttu-id="d41de-118">Unterdrückt die Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="d41de-118">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="d41de-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d41de-119">-Name</span></span>
<span data-ttu-id="d41de-120">Gibt den Namen der zu entfernenden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="d41de-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="d41de-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d41de-121">This parameter is required.</span></span>
<span data-ttu-id="d41de-122">Bei diesem Parameterwert wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="d41de-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="d41de-123">Platzhalterzeichen sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d41de-123">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="d41de-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="d41de-124">-Profile</span></span>
<span data-ttu-id="d41de-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d41de-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d41de-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d41de-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d41de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41de-127">CommonParameters</span></span>
<span data-ttu-id="d41de-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d41de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41de-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d41de-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41de-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d41de-130">INPUTS</span></span>

### <span data-ttu-id="d41de-131">Keine</span><span class="sxs-lookup"><span data-stu-id="d41de-131">None</span></span>
<span data-ttu-id="d41de-132">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="d41de-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d41de-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d41de-133">OUTPUTS</span></span>

### <span data-ttu-id="d41de-134">None oder System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d41de-134">None or System.Boolean</span></span>
<span data-ttu-id="d41de-135">Wenn Sie den Parameter *passthru* verwenden, gibt dieses Cmdlet einen booleschen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d41de-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="d41de-136">Andernfalls gibt Sie keine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="d41de-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="d41de-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d41de-137">NOTES</span></span>

## <span data-ttu-id="d41de-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d41de-138">RELATED LINKS</span></span>

[<span data-ttu-id="d41de-139">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d41de-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="d41de-140">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d41de-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="d41de-141">Satz-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d41de-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


