---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 6396da138a0bafd54241f859c107601a1ce14b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935459"
---
# <span data-ttu-id="17213-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="17213-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="17213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17213-102">SYNOPSIS</span></span>
<span data-ttu-id="17213-103">Erstellt/aktualisiert ein DataLake gen2-Element-ACL-Objekt, das in einem Update-AzDataLakeGen2Item verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="17213-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="17213-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17213-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="17213-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17213-105">DESCRIPTION</span></span>
<span data-ttu-id="17213-106">Das **Cmdlet Set-AzDataLakeGen2ItemAclObject** erstellt/aktualisiert ein DataLake gen2-Element-ACL-Objekt, das in einem Update-AzDataLakeGen2Item verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="17213-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="17213-107">Wenn der neue ACL-Eintrag mit demselben AccessControlType/EntityId/DefaultScope nicht in der Eingabe-ACL vorhanden ist, wird ein neuer ACL-Eintrag erstellt, sonst wird die Berechtigung des vorhandenen ACL-Eintrags aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="17213-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="17213-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17213-108">EXAMPLES</span></span>

### <span data-ttu-id="17213-109">Beispiel 1: Erstellen eines ACL-Objekts mit 3 ACL-Eintrag und Aktualisieren der ACL in einem Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="17213-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="17213-110">Mit diesem Befehl wird ein ACL-Objekt mit drei ACL-Einträgen erstellt (verwenden Sie den Parameter -InputObject, um dem vorhandenen acl-Objekt einen acl-Eintrag hinzuzufügen), und aktualisiert die ACL in einem Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="17213-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="17213-111">Beispiel 2: Erstellen eines ACL-Objekts mit vier ACL-Einträgen und Aktualisieren der Berechtigung eines vorhandenen ACL-Eintrags</span><span class="sxs-lookup"><span data-stu-id="17213-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

<span data-ttu-id="17213-112">Mit diesem Befehl wird zuerst ein ACL-Objekt mit vier ACL-Einträgen erstellt, und dann wird das Cmdlet erneut mit einer anderen Berechtigung, aber demselben AccessControlType/EntityId/DefaultScope eines vorhandenen ACL-Eintrags ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17213-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="17213-113">Anschließend wird die Berechtigung des ACL-Eintrags aktualisiert, aber kein neuer ACL-Eintrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="17213-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="17213-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="17213-114">PARAMETERS</span></span>

### <span data-ttu-id="17213-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="17213-115">-AccessControlType</span></span>
<span data-ttu-id="17213-116">Es gibt vier Typen: "Benutzer" gewährt dem Besitzer oder einem benannten Benutzer Rechte, "Gruppe" gewährt der besitzenden Gruppe oder einer benannten Gruppe Rechte, "mask" schränkt rechte ein, die benannten Benutzern und den Mitgliedern von Gruppen gewährt werden, und "andere" gewährt Allen Benutzern Rechte, die in keinem der anderen Einträge gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="17213-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17213-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="17213-117">-DefaultScope</span></span>
<span data-ttu-id="17213-118">Legen Sie diesen Parameter so ein, dass der #A0 zur Standard-ACL für ein Verzeichnis gehört. andernfalls ist der Bereich implizit, und der ACE gehört zur Zugriffs-ACL.</span><span class="sxs-lookup"><span data-stu-id="17213-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17213-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="17213-119">-EntityId</span></span>
<span data-ttu-id="17213-120">Der Benutzer- oder Gruppenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="17213-120">The user or group identifier.</span></span>
<span data-ttu-id="17213-121">Es wird für Einträge von AccessControlType "mask" und "other" nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="17213-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="17213-122">Der Benutzer- oder Gruppenbezeichner wird auch für den Besitzer und die besitzende Gruppe nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="17213-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17213-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17213-123">-InputObject</span></span>
<span data-ttu-id="17213-124">Wenn Sie das PSPathAccessControlEntry-Objekt eingeben, wird die neue ACL als neues Element des Eingabeobjekts \[ \] PSPathAccessControlEntry \[ \] hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="17213-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17213-125">-Permission</span><span class="sxs-lookup"><span data-stu-id="17213-125">-Permission</span></span>
<span data-ttu-id="17213-126">Das Berechtigungsfeld ist eine Drei-Zeichen-Sequenz, bei der das erste Zeichen "r" lautet, um Lesezugriff zu gewähren, das zweite Zeichen ist "w", um Schreibzugriff zu gewähren, und das dritte Zeichen ist "x", um die Ausführungsberechtigung zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="17213-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="17213-127">Wenn der Zugriff nicht gewährt wird, wird das Zeichen "-" verwendet, um zu bezeichnen, dass die Berechtigung verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="17213-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17213-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17213-128">CommonParameters</span></span>
<span data-ttu-id="17213-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17213-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17213-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17213-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17213-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17213-131">INPUTS</span></span>

### <span data-ttu-id="17213-132">Keine</span><span class="sxs-lookup"><span data-stu-id="17213-132">None</span></span>

## <span data-ttu-id="17213-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17213-133">OUTPUTS</span></span>

### <span data-ttu-id="17213-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="17213-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="17213-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="17213-135">NOTES</span></span>

## <span data-ttu-id="17213-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="17213-136">RELATED LINKS</span></span>
