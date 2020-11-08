---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005909"
---
# <span data-ttu-id="ac2c8-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="ac2c8-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="ac2c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac2c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ac2c8-103">Entfernt Objekte in Azure Active Directory, die Azure RemoteApp-virtuellen Computern zugeordnet sind, die nicht mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="ac2c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac2c8-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac2c8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac2c8-105">DESCRIPTION</span></span>
<span data-ttu-id="ac2c8-106">Mit dem Cmdlet " **Clear-AzureRemoteAppVmStaleAdObject** " werden Objekte in Azure Active Directory entfernt, die Azure RemoteApp-virtuellen Computern zugeordnet sind, die nicht mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="ac2c8-107">Sie müssen Anmeldeinformationen verwenden, die Rechte zum Entfernen von Azure Active Directory-Objekten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="ac2c8-108">Wenn Sie den allgemeinen Parameter *verbose* angeben, zeigt dieses Cmdlet den Namen jedes gelöschten Objekts an.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="ac2c8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac2c8-109">EXAMPLES</span></span>

### <span data-ttu-id="ac2c8-110">Beispiel 1: Löschen veralteter Objekte für eine Sammlung</span><span class="sxs-lookup"><span data-stu-id="ac2c8-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="ac2c8-111">Der erste Befehl fordert Sie auf, einen Benutzernamen und ein Kennwort einzugeben, indem Sie **Get-Credential** verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="ac2c8-112">Der Befehl speichert die Ergebnisse in der $AdminCredentials-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="ac2c8-113">Mit dem zweiten Befehl werden die veralteten Objekte für die Sammlung mit dem Namen "Contoso" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="ac2c8-114">Der Befehl verwendet die in $AdminCredentials Variablen gespeicherten Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="ac2c8-115">Damit der Befehl erfolgreich ausgeführt werden kann, müssen diese Anmeldeinformationen über die entsprechenden Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="ac2c8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac2c8-116">PARAMETERS</span></span>

### <span data-ttu-id="ac2c8-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="ac2c8-117">-CollectionName</span></span>
<span data-ttu-id="ac2c8-118">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac2c8-119">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="ac2c8-119">-Credential</span></span>
<span data-ttu-id="ac2c8-120">Gibt eine Anmeldeinformation an, die Rechte zum Ausführen dieser Aktion aufweist.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="ac2c8-121">Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="ac2c8-122">Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet die aktuellen Anmeldeinformationen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac2c8-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="ac2c8-123">-Profile</span></span>
<span data-ttu-id="ac2c8-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ac2c8-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ac2c8-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac2c8-126">-Confirm</span></span>
<span data-ttu-id="ac2c8-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac2c8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac2c8-128">-WhatIf</span></span>
<span data-ttu-id="ac2c8-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac2c8-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac2c8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac2c8-131">CommonParameters</span></span>
<span data-ttu-id="ac2c8-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac2c8-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac2c8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac2c8-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac2c8-134">INPUTS</span></span>

## <span data-ttu-id="ac2c8-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac2c8-135">OUTPUTS</span></span>

## <span data-ttu-id="ac2c8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac2c8-136">NOTES</span></span>

## <span data-ttu-id="ac2c8-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac2c8-137">RELATED LINKS</span></span>

[<span data-ttu-id="ac2c8-138">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="ac2c8-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


