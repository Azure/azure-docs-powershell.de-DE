---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006427"
---
# <span data-ttu-id="0524e-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0524e-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="0524e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0524e-102">SYNOPSIS</span></span>

<span data-ttu-id="0524e-103">Erstellt eine Anmeldeinformationen in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="0524e-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="0524e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0524e-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0524e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0524e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0524e-106">Das Cmdlet **New-AzureAutomationCredential** erstellt eine Anmeldeinformationen als **PSCredential** -Objekt in der Microsoft Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="0524e-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="0524e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0524e-107">EXAMPLES</span></span>

### <span data-ttu-id="0524e-108">Beispiel 1: Erstellen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="0524e-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="0524e-109">Mit diesen Befehlen werden die Anmeldeinformationen mit dem Namen myCredential erstellt.</span><span class="sxs-lookup"><span data-stu-id="0524e-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="0524e-110">Zuerst wird ein Anmeldeinformationsobjekt erstellt, das einen Benutzernamen und ein Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="0524e-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="0524e-111">Dieser wird dann im letzten Befehl verwendet, um die Automatisierungs Anmeldeinformationen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0524e-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="0524e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0524e-112">PARAMETERS</span></span>

### <span data-ttu-id="0524e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0524e-113">-AutomationAccountName</span></span>
<span data-ttu-id="0524e-114">Gibt den Namen des Automatisierungs Kontos an, in dem die Anmeldeinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0524e-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

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

### <span data-ttu-id="0524e-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0524e-115">-Description</span></span>
<span data-ttu-id="0524e-116">Gibt eine Beschreibung für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="0524e-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="0524e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0524e-117">-Name</span></span>
<span data-ttu-id="0524e-118">Gibt einen Namen für die Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="0524e-118">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="0524e-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="0524e-119">-Profile</span></span>
<span data-ttu-id="0524e-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0524e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0524e-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0524e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0524e-122">-Wert</span><span class="sxs-lookup"><span data-stu-id="0524e-122">-Value</span></span>
<span data-ttu-id="0524e-123">Gibt die Anmeldeinformationen als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0524e-123">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="0524e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0524e-124">CommonParameters</span></span>
<span data-ttu-id="0524e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0524e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0524e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0524e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0524e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0524e-127">INPUTS</span></span>

## <span data-ttu-id="0524e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0524e-128">OUTPUTS</span></span>

### <span data-ttu-id="0524e-129">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="0524e-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="0524e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0524e-130">NOTES</span></span>

## <span data-ttu-id="0524e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0524e-131">RELATED LINKS</span></span>

[<span data-ttu-id="0524e-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0524e-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="0524e-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0524e-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="0524e-134">Satz-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0524e-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


